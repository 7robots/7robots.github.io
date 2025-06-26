---
layout: default
title: Internet2 7 Mar 2024
parent: agora
---
# Internet2 7 Mar 2024

## Building a NetDevOps Team

- Definitions
   - NetDevOps
   - Network Automation
- CI
   - Let my engineer add a new BGP neighbor into the file, press a button to launch scripts, press a button to deploy, press a button to verify environment afterwards
- CD
   - Missed her definition
- Team structures
   - Software development team
   - Network engineering team
   - Systems teams
- NetDevOps
   - Varying team sizes
   - Teams with more than 1 skill set
   - Break down silos
   - Collaboration between software, systems, and network
- ASU
   - Campus Perspective
      - Large campus of 50k students
         - 90 different platforms
         - 3000 wired devices
         - 11k AP
      - Challenges
         - Security
         - Diversity
         - Scalability
         - Global configuration consistency
   - Where do I start?
      - Scale of infra was too much
      - Idea of a network engineer who programs was not foreign — old automation scripts, not well understood
      - A programming person sounds like a good idea for our backfill
         - Repurpose network engineer?
         - Force network engineer to take on new responsibilities?
         - Hire?
   - Attempt 1
      - Determine specific goals for position
         - Automate device image upgrades
         - Locate underutilized infrastructure
         - Standardized config
         - Repetitive (boring) work
      - Rewrote job description
         - Shift priority from networking
         - More programming and automation
      - Things that went well
         - Foundation of a source of intent
         - Major accomplishments
            - Automated image upgrade tooling
            - Automated device onboarding into netbook
            - Mass config changes
            - Project-specific config deployments
            - IP helper migrations
            - Report generation
            - Maturity of automation rose
      - Things that did not go well
         - Automation engineers hopped projects without documenting
         - Time estimates weren’t good
         - Workload of engineers shifted to others to focus on automation
         - Automation team didn’t know how to work “agile”
         - Eventually lost staff to other opportunities
   - Attempt 2:
      - Formed a real team
      - Proposed new positions at different skill levels
      - New pillar within network services to focus on NetDevOps
      - Utilized a current staff member to function as team lead
      - Outline plans to train current network engineers
         - Dedicated time for training
         - Knowledge transfer
         - Set aside training budgets
      - Engage your senior leadership
         - Provide examples
         - Highlight benefits
         - Discuss emerging trends
- GlobalNOC
   - Been doing network automation for a while
   - We already had a team working and running OESS
      - That was the core of the team
   - The NAP team (also responsible for perfSONAR)
   - 3 people were essentially already doing this sort of thing
   - SysEng was already DevOps
      - Both operations and evelopemtn
      - Try to hire well rounded individuals with both scripting and automation
      - Network knowledge not a requirement
   - Requirements and Design Phase
      - Interact with network engineers — get right set of requirements
      - SCRUM
      - Lead network person to communicate with other teams, onboard customers
   - GNAT and GSCS — both network automation tools
      - Fill in the box templates that translate into device specific syntax (that can be viewed)
   - Policies and Consistency for engineers
      - Code policies
      - Service policies
   - Software engineers shouldn’t be expected to understand advanced network concepts
      - Rely on more senior engineers
      - Rely on network engineers to understand their networks
      - Foster communications between SysEng and NetEng
      - Success on smaller projects led to a new class of engineer that could tackle bigger automation projects
   - Community - Software Super Users
      - Class of network engineers inside GlobalNOC
      - This person interacts with SysAeng to get assistance in aPI’s, writing scripts
      - Network operations automation versus configuration automation
- Mike S (what I wish you knew about NetDevOps)
   - It’s not new! (Mythical man month, agile software development in 2001, CI/CD movements going back to 2007, lean methodology back to the 50’s)
   - Requirement
      - Be willing not to do dumb things
      - We do dumb things all the time — it’s easy
      - Recognize that in intense, rapid, unceasing change, doing dumb things will increase
      - So … aspire to do better
   - Ways to do it wrong
      - Temporary cross-functional teams, sliced from real teams
   - doit right
      - Instead — build permanent cross-functional teams oriented around what it takes to completely deliver a service or suite of related services
   - Shorter your control loops to match the rate of change of the thing you need to control
      - Minimize barriers to communication and coordination
      - Drive locus of control out to the leaves of the tree (self-service)
      - Don’t take too long to implement an old requirement
   - Pay attention to the only supply chain that matters
      - Sourcing awesome people
      - Get good people, develop them retain them
   - build NetDevOps
      - A couple of network, a couple of system, a couple of software
      - Or
      - people who have occupied multiple roles (both network and system)
      - Both system and software
      - Both network and software

## AI Panel (me, Brandon, Erin, Don)

- Questions

   ◦	Lots of IT leaders in higher ed are interested in generative AI, and trying to figure out the role of an IT organization is in this era.  **What do you see as the role of your organization, and what are your goals for generative AI at your institution?**

   ◦	Building on that, we discussed a little last night about the concept of ROI, and you each said, to some extent, that it cannot really be quantified right now.  **How do you measure success, and what will determine if these efforts continue to grow?**

- (prompt for Don's story from faculty, also the 3-year clock)

   ◦	Conventional wisdom says that running AI services is quite expensive, with a lot of potential costs in both the initial and runtime stages of an implementation.  So one thing that many folks in this room will be wondering is **how do you pay for this?**

   **▪	(**Jefferson mentioned Dean support, innovation fund)

   ▪	(Don mentioned provisioned throughput – no special infusion from MS, market rates)

   ▪	(Erin mentioned grant writing)

   ◦	Let's broaden that – **how are you resourcing this effort** from the perspective of people skills?  How big are your teams, what skills do they need to have, and how are you growing that capability?

   ▪	(Erin talked about expanding her team)

   ▪	(Jefferson mentioned upskilling particular roles)

   ◦	I also know **strategic partnerships**, particular with cloud providers, are playing a role in your rollout of generative AI services.  Can you describe how that is working, and how you have gone about growing those relationships?

   ▪	(prompt for Erin re: AWS)

   ◦	Let's pivot a bit.  We know that AI means many things to different groups: research, administrative, students, faculty.  How are you **engaging with campus** constituents, facilitating conversations, and promoting AI literacy?

   ▪	(prompt for jefferson, don re: communities of practice)

   ◦	How are you connecting with **faculty**?  What venues exist or have you created to be involved in conversations about classroom tools, pedagogical shifts?

   ◦	How do you talk about this to **university leadership**?  When you do, what are your goals in those conversations?

   ▪	(Erin mentioned addressing the board)

   ◦	Audience Q&A (could go after the last question)

   ◦	What advice would you give to the folks in the room wondering **where they should start?**

   ◦	don't forget – slack invite

