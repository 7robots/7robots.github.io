# CLAUDE.md - Project Context for Claude Code

## Project Overview
This is a Jekyll static site using the **Just the Docs** theme, hosted on GitHub Pages at `commonplace.7robots.org`. It's a personal commonplace book (digital knowledge management system) with collections of quotes, conference notes, meditations, and other curated content.

## Site Structure

### Main Sections (nav_order)
1. **home** (index.md) - Main landing page
2. **hypomnemata** - Book quotes and literary excerpts
3. **selene** - Lunar science
4. **polis** - Local history (Harvard, MA)
5. **agora** - Conference notes and lectures
6. **techne** - Technical notes
7. **anthologia** - Interesting articles
8. **melete** - Meditations from "Savor" by Thich Nhat Hanh

### Key Configuration (_config.yml)
- Theme: `just-the-docs`
- Color scheme: `dark`
- Custom callouts defined for each section with unique colors

## Just the Docs Patterns

### Frontmatter for Section Home Pages
```yaml
---
layout: default
title: section-name
nav_order: N
has_children: true
has_toc: false  # Disable auto-generated child list
---
```

### Frontmatter for Child Pages (hidden from nav)
```yaml
---
layout: default
title: "Page Title"
parent: section-name
nav_exclude: true
nav_order: N
---
```

### Links
- **Do NOT include `.md` extension** in links
- Relative links work in lists but had issues in tables
- Use relative links like `(Page-Name)` from section home pages

## Important Lessons Learned

### Case Sensitivity Issue
- **Problem**: macOS filesystem is case-insensitive, but GitHub Pages (Linux) is case-sensitive
- **Symptom**: Files tracked in git as lowercase (`two-moons.md`) but links expected capitalized (`Two-moons`) caused 404 errors
- **Solution**: Use `git mv` to fix case: `git mv lowercase.md Capitalized.md`
- **Check for issues**: Compare `git ls-files` output with `ls` output

### Markdown Tables vs Lists
- Tables work fine once case sensitivity issues are resolved
- hypomnemata uses a table format sorted by book title
- agora uses lists grouped by topic

### File Naming
- Use hyphens instead of spaces in filenames
- Files with spaces require `%20` URL encoding
- Special characters (curly apostrophes `'`) should be avoided; use straight apostrophes `'`

## Content Migration (from Craft)

Source content was at `/Users/olmy/Documents/episteme`. Migration involved:
1. Adding Just the Docs YAML frontmatter to all files
2. Fixing image paths to absolute paths (`/hypomnemata/assets/...`)
3. Copying asset folders alongside markdown files
4. Normalizing special characters (curly to straight apostrophes)

## hypomnemata Page Structure

Each quote page follows this structure:
```markdown
---
layout: default
title: "Quote-Title"
parent: hypomnemata
nav_exclude: true
nav_order: N
---
## Author: Author Name
Book: Book Title
Subject: Fiction|Poetry|Religion|etc.

# Readable Quote Title

[Quote text here]

![image](image-path)

Image caption
```

## Build & Deploy
- GitHub Actions workflow builds and deploys on push to main
- Build uses Ruby 3.3 and Jekyll 4.3.3
- Workflow files in `.github/workflows/`

## Commands Reference

```bash
# Check for case sensitivity issues
git ls-files hypomnemata/*.md | sort > /tmp/git.txt
ls hypomnemata/*.md | sort > /tmp/disk.txt
diff /tmp/git.txt /tmp/disk.txt

# Fix case in git
git mv oldname.md Newname.md

# Local build (requires Ruby 3.3+)
bundle install
bundle exec jekyll build
```
