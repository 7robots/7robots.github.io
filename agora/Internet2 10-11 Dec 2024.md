---
layout: default
title: Internet2 10-11 Dec 2024
parent: agora
---
# Internet2 10-11 Dec 2024

## IPv6-only on LHC at CERN
* Summary:
	* The WLCG, a global computing grid for high-energy physics, is transitioning to IPv6 due to IPv4 exhaustion and security concerns.  The HEPIX IPv6 WG has been instrumental in this transition, with most storage now dual-stack and a goal to make all WLCG services dual-stack.  While IPv6-only networks are being implemented, challenges remain, including complex configurations and a lack of local expertise.
* Salon G
* Agenda:
	* WLCG
	* IPv6 requirement and HEPIX IPv6 WG
	* Phases
	* IPv6 in 2024 data challenge
* WLCG (worldwide LHC computing grid)
	* More than 170 computing centers
	* Sites in 3 tiers
		* Tier 0 CERN
		* Tier 1 national laboratories
		* Tier 2’s 160 university physics dpeamrnts
	* 2 network
		* HHCOPN (private optical)
		* LHCONE (L3vpn, vrf)
* Infra administration
	* HHCOPN and LHCONE coordinated by CERN and NREN’s
	* Other IP network managed by NRENS
	* Campus network infrastructure managed locally
* why interest in IPv6 13 years ago?
	* Some sites running out of IPv4
	* Surveyed for IPv6 readiness
	* Factors
		* Opportunistic deployments
		* Middleware and software often not v6 capable le
		* Performance: avoide NAT’s proxies 
	* more recent reasons to deploy v6
		* US government directive M-21-07 — applies to WLCG facilities at Fermilab and Brookhaven
	* SciTags — accountability for traffic
		* Per flow labels for science
	* Slow pace of IPv6 deployment in R&E networks
		* NREN. Backbones have been dual stack since early 2000’s
		* Campuses well behind ISPs
* HEPIX IPv6 WG
	* Assistant nd drive WLCG adoption of IPv6
	* Chaired by Dave Kelsey
	* Phase 1 (2011-2016)
		* Analysis of work
		* Review of apples, middleware, systems, tools, security
		* Creation and operation of a distributed test bed
	* Phase 2 (2017-2023)
		* Enabling IPv6 storage (tier 2 storage)
		* Almost 100% is now dual stack
		* Slow and steady
	* Phase 3 IPv6 only (started in 2019)
		* Goal to simplify complexity and streamline security
		* Positive examples of worldwide infra (like facebook) that IPv6 only
			* But FB is monolithic
		* To bey IPv6 only would have to expand to worker nodes (this is harder)
* IPv6 only WN’s and Ce’s
	* 63% of in scope worker nodes now dual stack and 23# in progress
* Issues reported
	* Delays where IPv6 migration is coupled iwth other projects
	* Some sites have complex configs with respec tot NAT and global IPv6
	* Other priorities (like CentOS EOL, new Auth tokens)
	* Concern that WN’s behind NAT would be more exposed
	* Lack of local expertise
	* 5% of sites have not responded
	* 9% on hold
* IPv6 and 9000 MTU
	* Throughput significantly improved by jumbo frames
	* Reasonable adoption at tier 1 and tier 2
	* IPv6 does not fragment on the path so Path MTU Discovery MUST allow 9000 MTU sites
* Other tools that support IPv6
	* Rubio
	* FTS
	* XrootD
	* HTConder
	* DCache
* Data Challenge (2 weeks in February 2024)
	* Overall throughput by experiment. Went well!
	* Achieved full throughput 2.4TB/s 
	* Moved about 180 petabytes
* Monitoring traffic
	* Grafana infra at CERN to do this
* IPv4 Spikes due to:
	* Heavier activity by v4 only clusters still shows up
	* IPv4 tests by services like personal
	* IPv4 only sites
	* IPv4 still preferred by dual stack sites
	* Something else
* V6 only goal
	* Suggested target “end of run 3” before LHC run 4 (starting around 2030)?
* Current status
	* Principles
		* Any sites can have IPv6 only clients and fully function in WLCG
		* Gradually moving all WLCG services to be fully dual stack
* SciTags
	* IPv6 only capability
	* Definined by WLCG WG
	* Allow NRENs or account for research traffic
	* Uses IPv6 flow labels
	* Written up as an IETF ID
	* New implementation in flows-go
* IPv6 mostly
	* WLCG is generally compute and storage, rather than user devices
	* For hosts and end user devices …
	* removing IPv4 where you can
	* New IETF ID
	* Hosts can negotiate to turn off IPv4 via DHCPv4 option 108
	* Support on android, Mac, IOS and soon Windows

## Lunch 12:10-1:40

## 1:40-2:30 Better Identity Matching thru Neural Networks
* Salon F
	* 

## Building an AI Chatbot at Internet2 10:45 - 11:20
* Summary:
	* Dd
* Karl Newell at Internet2
* Overview of technologies used
	* RAG
	* Bedrock + KnowledgeBase
* First attempt
	* Local LLM using Ollama and models from Hugging Face
* Hosted LLMs in Bedrock
	* Claude, Llama 3, Mistral
	* Embedding models (document to vector dB)
	* Easy to switch between models
	* Data is not used to train models
	* Amazon Q
* Another experiment
	* LangChain + Streamlit
* Open Source AI assistant based on Danswer/Onyx
	* Pre-built RAG application
	* Connect to data sources like:
		* Web
		* Confluence
		* Google drive
		* Salesforce
		* Many more
* Other experiments
	* ReAct (not the JS framework)
		* Reason + Act
		* Agentic framework
	* RAFT
		* Retrieval augmented fine tuning
* 

## AI Chatbots and Research Concierge Services 10:20-10:45
* Summary:
	* Lehigh University is developing vendor-agnostic, sustainable chatbots with a focus on data minimization and feedback loops. The chatbots, powered by a multi-index knowledge base, aim to assist researchers with grant information, equipment, and research at Lehigh.
* Salon E
* Lehigh University
* Goals:
	* Vendor agnostic
	* Develop sustainable chatbots
	* IaC
	* Data minimization
	* Feedback loop
	* Provide analytics data for chatbots
	* Data source supported:
		* PDFs
		* Websites
		* Confluence
* Types of chatbots:
	* Agents on websites
		* LTS (completed)
		* HR (completed)
		* Auxiliary services (dining, housing, transportation, purchasing, etc) (completed)
	* Research concierge service
		* Phase 1: index and train model on our policies (PDF) (completed)
		* Phase 2: index and train model on funding agencies
			* Grant policies
			* Grants - match researcher with possible grants (probably with web crawler)
		* Phase 3: index and train model on equipment and research being done at Lehigh
	* Architecture
		* React/Node -> API Gateway -> Lambda -> Bedrock -> KnowledgeBase -> Crawlers -> sites to be indexed
		* Visualization
			* QuickSight dashboards
			* Chatbots analytics data
			* Lambda
			* SQS (SQS takes in events from the chatbot’s lambda)
		* Note: in knowledge base, you can have multiple indexes
	* What data is collected
		* Conversations
		* Interactions
		* ResponseSources
* Lessons learned
	* Develop micro services
	* OpenSearch and Kendra are expensive
	* Models constantly changing
	* To stream or not to stream
	* Get your system prompt right
	* Fine tune temperature
	* Getting CoRS right with the API gateway
	* Clean up your data

## 

## Multi-lateral Federation for Research: REDCap, OpenOnDemand, and Beyond
* Summary:
	* The Multi-lateral Federation for Research session discussed the use of Cirrus Identity Proxy for research institutions.  Texas A&M and UNC at Chapel Hill shared their experiences implementing Cirrus to address challenges with research applications and guest access.  Future developments for Cirrus Identity include focused deployments, improved user support, and metadata management.
* Salon C/D
* Texas A&M, UNC at Chapel Hill, and Cirrus Identity
* Use case: research, service provider challenges with multilateral federation
	* Solution: Cirrus Identity Proxy
		* Hosted and managed solution that supports eduGAIn multilateral federation
		* In common, Google, MS, LinkedIn, Amazon, Apple, ORCID, Cirrus Identty OrgBrandedID
		* Guides institutions thru implementation and streamlines transition to cloud-hosted solution
	* Discovery Screen (IDP selector)
* High-level architecture
	* Cirrus Account linking and Cirrus Auth Proxy in the middle
		* IDmS, IDP, apps at edges
* A&M Use Case (Garrett Yamada)
	* Didn’t want to use their on-prem Shibboleth environment, not well maintained any more
	* Use Cirrus Identity Proxy to facilitate access to Huron application suite for division of research
	* Perform self-service conflict of interest checks
	* Didn’t have to setup a sponsored NetID for everyone outside campus
	* Display large portion of TAMU IDP choices
	* Lessons learned
		* Attribute standardization matters a lot
		* Not that many A&M system members were also InCommon. This is changing.
* UNC Chapel Hill Use Case (Tien and Yann)
	* REDCap: Research Electronic Data Capture
	* Federation journey for REDCap at HUN
	* Pre-SSO headaches — multiple REDCap sites, each with their own user database, users had multiple accounts, big admin and UX burden
	* Non UNC SSO headaches
		* Home brew: registered REDCap SP’s with InCommon R&S category and doing a home brew entity discovery service
		* Painful and lots of labor
		* I just want to admin REDCAP, not become an IaM team
	* Guest SSO
		* I went crazy too many people wanted to use our REDCap instances
	* 3 pain points
		* External users logging with their own accounts
		* Less work sessions up IDPS
		* Streamline guest onboarding
	* Architecture
		* Cirrus Auth Proxy in the middle
		* Cirrus Discovery on the side
		* REDcap instances as apps
		* Various IDP’s that connect to Auth proxy
	* Lessons learned:
		* Proxy makes it easier for external users to login, they’re using accounts they trust, external accounts managed in 1 place, removing work from REDCap admins
		* Less work setting up IDP’s - proxy + SAML, 
		* Less admin work to support SP’s behind proxy
		* Guest users process streamlined
* Cirrus Identity Futures
	* Theme 1: Identity proxy
		* Deliver focused deployments for research oriented use cases
		* New and better options to provide end user support
		* Better support for metadata management (self-service and broader entity categories support)
	* Theme 2: Identity Bridge
		* Scale, reduce time to deploy, reduce effort administer Cirrus Bridge for EntraID and Okta
		* Evaluate options beyond Entra and Okta
		* Repeat: better support for metadata management
	* Theme 3: engage with community
		* Engage with R&E
		* Support login.gov integrations
		* Emerging MFA requirements of federal agencies
* Note: there is a past presentation on Internet2 on Dynamic MFA

## AI as a Service 8:30-8:55
* Summary:
	* The University of Florida’s Navigator AI project aims to provide a unified AI platform for students, faculty, and staff. The project, starting with an AI gateway, offers various services including a chatbot, vector databases, and data pipelines, with a focus on security, governance, and user-friendliness.
* Salon E
* University of Florida IT, Mehdi Ramdane and Nick Cecere
* Navigator AI for UF students, faculty, and staff
* How did it start?
	* Fragmented and non-specific requests for AI
	* Various data types
	* Different levels of users
	* Use case by use case
* Approach 
	* What is variable and less variable
	* Variable, not a sprint
	* Security and governance on day 1
	* Local AI offering should be easier and faster than commercial
	* Insert an AI gateway (API-based) between applications and models
* How it started
	* Start with the gateway outwards
	* Various data types (open, sensitive, restricted)
	* Multiple user types (from hobbyist to expert)
	* Stayed clear of restricted data types like HIPAA, ITAR, PCI, etc but FERPA yes
* Strategy
	* Services that open up additional use cases
		* API gateway
		* Vector databases
		* Data pipelines
* Navigator Chat
	* First major use case
	* Based on LibreChat
	* 24 LLMs, 2 image generation models (flux and stable diffusion)
		* OpenAI, Anthropic, Google, Meta, nvidia
	* use UF one data 
	* Llama is 30%, 21% is gpt-4o, gpt-4-turbo, everything else is less than 10%
* Navigator Toolkit
	* Based on web-frontend to LiteLLM
	* Tools for faculty, students, staff to work with API’s to work with AI
	* Integrate any application that supports OpenAI SDK
	* It supports both local and cloud models
	* Self-service API key generation available to everyone
	* Budget of $5 per month
		* 10 million tokens per month
		* 7.5 million pages of words
* Model Review once per semester
* Navigator Assistant
	* Web assistants (openwebUI)
* What’s next
	* VectorDB as a service
	* STT using Whisper
	* Chat 3.0

## Scalable Mgmt of VPCs 4-4:20 Salon G
* Summary: 
	* VPCs offer scalable and flexible virtual networks with customizable CIDR and security features. Design patterns like mesh, hub and spoke, and VPC lattice provide isolation and service sharing. Firewall strategies, such as centralization, depend on cloud topology and practicality.
* Joseph Rafferty at A&M
* Primer
	* Definition of VPC
	* Virtual network dedicated to your account
	* Customizable: CIDR
	* Deny by default
	* Scalable and flexible (create multiple vpc’s to add more logical isolation
	* Scales to match your infra
	* SG’s
		* Deny by default
	* NACL’s
		* Allow by default
	* Inbound and outbound rules
	* No broadcast traffic, no layer 2 threat
* VPC patterns
	* Mesh - every VPC connects to every other, as necessary
		* Peerings can explode in complexity as the VPC count increases
		* CIDR coordination important
	* hub and spoke
		* With shared services in the hub
		* Note: the VPC in the middle isn’t transitive
	* hub and spoke with TGW
		* Has route tables, can transit traffic
		* Trade-off is cost
	* VPC lattice
		* Leave most isolated
		* VPC lattice service network
		* This “pulls” specific services from a VPC to make it available to other VPC’s
			* Not too dissimilar to exposing an endpoint
* VPC Design
	* Shared VPC
		* Multiple apps in VPC with multiple linked accounts
		* Public and private subnets would span multiple accounts in the shared VPC
	* account-specific VPC’s
* Firewalls
	* Cloud topology differs from on-premises
	* Centralize or not centralize?
	* What’s possible, what’s practical
	* Possible to centralize both Ingres and egress with a central VPC

## Protecting R&E data protection in the quantum age
* Summary: 
	* Quantum computing poses a significant threat to traditional encryption methods, particularly asymmetric cryptography used for key agreement and authentication. To mitigate this risk, a multi-layered approach is needed, including quantum key distribution (QKD) for secure key exchange and post-quantum cryptography (PQC) algorithms for data encryption. Nokia is actively involved in developing quantum-safe networks, incorporating QKD, PQC, and a defense-in-depth strategy to protect against future quantum threats.
* Chris Janson, Nokia
* Agenda
	* Securing R&E data in the quantum era
	* Q day and quantum threats
	* Case study: how HellasQCI evaluated quantum protection
	* Quantum safe networking framework
* Relevant Threat Vectors (mostly re: network transmission)
	* Eavesdropping (confidentiality breached)
	* Man-in-the-middle (integrity compromised)
	* Denial of service (availability lost)
* Quantum eavesdropping
	* Unauthorized fiber tap
	* Adversarial optical demux and store
	* Could harvest now and decrypt later
	* Future sate: quantum computer and quantum algorithms
* Quantum Man in the Middle
	* Nothing unique to quantum
	* Intruding switch or server providing bad packets or info
* DoS attack
	* Injecting illiterate traffic to overwhelm
	* Nothing unique to quantum
* Today’s focus will mostly be on eavesdropping (confidentiality breached)
* The Threat: Q-Day
	* A cryptographically relevant quantum computer (CRQC) becomes available
	* Researchers have estimate of number of qubits needed
	* Technology is rapidly advancing
	* Not a question of if, but when
* IBM Quantum
	* Heron: 100 X n qubits classical + quantum intelligent orchestration
	* Flamingo (1000 qubits) communication/networking for quantum
	* Kookaburra (10,000 qubits) long range for practical error correction
	* Bluejay (100k qubits) further system scaling and integration
* When does a CRQC become real?
* Quantum computers would break widely-used asymmetric crypto
	* Mostly used for key agreement, authentication
	* E.g. TLS, IPSec, VPN, algorithms like RSA, ECC
	* Threat: Shor’s Algorithm

* Symmetric crypto
* symmetric crypto is still safe
	* Bulk data encryption
	* AES, ChaCha (key distribution)
	* Note: quantum threat to symmetric crypto would be based on Grover’s Algorithm

* Key Distribution
	* Pre-shared keys (manual or automated) still safe
	* Quantum Key Distribution (key distribution channel secured by quantum physics) still safe
	* Key agreement / exchange - key distribution channel secured by asymmetric crypto (this will get broken)
* Ingredients of Quantum safe networks
	* Keys (generation, strength) 
		* true random numbers assure key quality, key strength, delivery method
	* Key rotation
	* Locks (encryption) data inflight protected connectivity
* The Threat
	* Harvest Now Decrypt Later
	* Bad actors are already collecting the data
	* Time to plan and deploy
		* New ciphers, new commercial products, system change-outs
* Quantum safe networks elements
	* Addition of quantum physics into OSI stack with quantum enhanced key distribution
	* Layered onto network transmission gear:
		* SLTE optical networking
		* Terrestrial optical networking
		* IP networking
		* Microwave networking
* European Quantum Communications Initiative
	* EuroQCI - secure quantum communication infrastructure spanning EU
	* All 27 EU member states and ESA
	* Terrestrial segment with fiber
	* Space segment based on satellites
	* Will be an integral part of IRIS2
* Example: Athens PoC Quantum Secure Network
* QKD (quantum key distribution)
	* Can be based on quantum entanglement (potentially at risk from heat)
* Note: Nokia is already selling devices for QKD
* Non-entanglement (prepare and measure) stack
	* IDQ
		* Fetch encryption requirements and distribute classical keys
		* Their services use this prepare and measure technique
	* Evolutions informs KMS on key requirements
	* Nokia devices
* Note: all of this QKD stuff only protects ONE layer of the stack
	* Protection against quantum computing attacks will need to hit most layers of the stack
* Post Quantum Ciphers (PQC)
	* FIPS 203: Crystals + Kyber (module lattic-based key encryption)
	* FIPS 204: Crystals + Dilithium (module based
	* FIPS 205 SPHINCS+ (stateless has based digital signature
	* Asymmetric Mathematics-based ciphers
	* Kyler is already being used by iMessage and AWS
	* PQC overcomes the fear of Shor’s algorithm
	* All of this is complementary to use of symmetric key distribution for network and physical
* Nokia Quantum safe Network
	* Pre-shared keys with manual symmetric distribution
	* Automated PSK with symmetric distribution
	* Quantum physics hybrid QKD distribution
* Even more future defense in depth approach
	* Layers: physical, Ethernet, network, mpls, IP layers
* 

## Re-imaging Student Experiences with Azure OpenAI Services
* Summary
	* Microsoft’s Dr. Elka Walsh discusses AI adoption in education, highlighting its potential for personalized learning, accessibility, and data protection.  AI Assistants are seen as valuable tools for students and educators alike.
* presentation by Microsoft, Dr Elka Walsh, Americas Higher Ed Transformation Lead
* Change Management
	* Technology changes at an exponential rate
	* Organizations change at a logarithmic state
* AI adoption stats
	* 80% of students say AI in university not fully meeting expectations
	* 75% of knowledge workers already using AI at work
	* 30 minutes saved a day
* Opportunities for AI in education
	* Personalized learning
	* Improve accessibility
	* Build AI literacy
	* Equip students
	* Defend at machine speed
	* Protect our data
	* Engage learners
	* Analyze data efficiently
* Tutor Assistant to enhance decision making skills
	* Metacognitive feedback much more effective than action feedback and no feedback
* AI Assistants
	* Education
	* Research
	* Operational Excellence
* 

## Rapid Automation App Development
* Summary:
	* GitLab-driven automation is used for rapid app development, covering locally developed, OSS, and commercial products. The process involves code versioning, containerization, security scanning, and deployment to multiple environments, all managed through a centralized CICD pipeline.
* Presentation by William and Mary 
* Nearly everything uses automation driven by GitLab
* Applications in scope
	* Locally developed (includes scheduled jobs)
	* OSS
	* Commercial products
* application platform
	* K8s in AWS
* cloud native
	* Containers, API’s, loosely coupled, automated
* containers
	* Version everything together
	* Server OS isolated from applications
	* Basic security’s cans before running
	* Software doesn’t have to be delivered in containers
* Build once and promote as validated
	* Multiple instances
		* Test
		* Prod
* can managed up to 300k containers
* Common API for all components
* Large ecosystem of tools
* Runs everywhere
* Container orchestration
* Process
	* Write code
	* Push to git
	* CICD pipeline
		* Trivy Scan
		* Build container image
		* Trivy scan again
		* Xeol scanner (version scanning — software bill of materials)
* CICD pipeline
	* Centrally managed
	* Repo owners include a 3 line snippet
	* No developer action with changes
* Controlling K8s
	* Workloads -> K8s (flux reads repos)
	* K8s manifests
	* Container registry
* version control
	* Project source code
	* Packaging scripts
	* Pipeline configuration
	* Expected running state
	* Secrets 
* Observability layout
	* Running application
	* Front-ended by traefik 
	* Grafana Loki for logging
	* Prometheus for metrics scraping
	* Grafana for developer log access
	* OpenCost+amazon tagging for FinOps

## Rocking the cloud migration to AWS
* **Summary**
	* Cloud migration to AWS faces challenges including vendor issues, internal strife, and technical hurdles.  To overcome these obstacles, a comprehensive plan involving detailed specifications, training, and team collaboration is essential.**
**
* **Jeffrey Solomon and Robert Larson** *Loyola Marymount University*

* vendor struggles
	* Sow confusion
	* Over promised, under delivered
* internal riffs
	* Documentation gaps
	* Fear of the unknown
	* Lack of training
	* The 
* Technical snafus
	* Legacy systems
	* Latency
	* Network needs
* communication breakdowns
	* Language inconsistency
	* Scope creep
	* PoC’s
* Partners
	* Push for detailed SoW’s and clear deliverables
* Planning
	* Conduct a through sound check
	* Integrations
	* Bandwidth and latency
	* Consider security
* team harmony
	* Build a shared vocabulary
	* Provide transparency
	* Provide training early
* Next Steps
	* Cut cost, not chords
	* optimize systems, FinOps
	* Fine tune security
	* banner re-architecture
	* VDI and VoIP

## Migrating Cloud-resistant Workloads
* Summary
	* Harvard’s cloud migration goals include cost reduction and moving cloud-resistant workloads to a hybrid cloud edge solution.  AWS Local Zones and Outposts, as well as Azure Stack, are being evaluated for their performance, limitations, and cost-effectiveness.  Network performance and compatibility with existing infrastructure are key factors in the evaluation process.
* Ben and Al
* Cloud Migration goals
	* First goal 50%
	* Revised goal shutdown 60 Ox
* Enterprise agreements
	* AWS
	* Azure
	* Google
	* OCI
* Cloud adoption percentages across CSP’s
	* AWS 80%
	* OCI 3.3% (barely turned on, already past GCP)
	* GCP 3.2%
	* Azure 12.6%
* New focus on cost reduction
	* Colo facility as primary datacenter
	* VMWare as virtualization platform
* What’s still in datacenter
	* Network
	* Telecoms
	* OT (the hardest to migrate)
	* SaaS endpoints
* Cloud-resistant workloads
	* Hybrid cloud edge as solution
* Problem statements
	* Data residency requirements to support regulated data
	* Low latency high throughput applications
	* Static IP
	* Unencrypted protocols
	* Datacenter costs
	* Vendor challenges
	* On-prem costs
	* Virtualization platform (VMWare cost increases with Broadcom)
* Approach
	* AWS Outposts
	* AWS Local Zones (AWS metro presence in 1 Summer)
	* Azure Stack (Azure Local Zone equivalent)
* PoC Testing
	* Test cases
	* Documentation
	* Test framework
	* Networking services
* Test Readout and Recommendations
	* Consolidated findings and recommendations and next steps
* AWS Local Zones
	* Design validation
	* Use case validation
		* EC2
		* ECS
		* RDS
	* Test Results
		* .5ms and 2.5gbit/sec (between Harvard and AWS local zone)
		* Good performance results
	* Lessons learned
		* VPC Service Link is slow
		* Don’t have latest instance types (like m5)
		* We successfully moved:
		* LogicMonitor
		* DrvyvIQ
		* K8s Rancher
		* Several thick client applications
* AWS Outpost (as VMware alternative)
	* Design validation
	* Use case validation
	* Test results look good for network performance and compatible with needs
	* No bare metal support on AWS Outpost
	* Several technical limitations due to lack of features in Outpost server
	* Services
		* EC2 (GP2 instances storage)
		* ECS
	* backup via cohesity not supported
	* Outpost Rack IS a full rack
		* Still paying for full rack and powering full rack (even if you only use some of it)
* Lessons Learned
	* Validat documented features
	* Build skills
* Recommendations
	* Could be an alternative to VMWare
	* Additional TCO required
	* Any use cases that cannot be validated on Outpost server could be validated on Outpost rack
	* Provisions for purchasing rack should include conditions on successful testing
* Azure Stack Goals
	* Design validation Use case
	* Use case validation
	* Services
		* Azure VDI
		* Azure site recovery 
		* Database
	* PoC going on right now
	* Observations
		* Time acquire try and buy took a long time
		* Lots of prereq work (Dell paperwork)
		* Much more reasonable hardware costs for full Azure Stack
		* Windows licensing portability
		* Existing windows admin and azure skills should make adoption easier
	* procurement of Azure Stack a lot more flexible than AWS Outposts
	* Observations
		* Vendor docs don’t tell whole story
		* Time consuming PoC
		* Metro cloud or AWs local zones require the lowest LoE
		* Managing edge requires merger of datacenter skills and cloud skills
		* High availability for edge has potential to be very expensive
		* Opportunity to better automate on-premises workloads using cloud native skills
		* Network is crucial for all of these solutions
		* Plug for I2 Cloud Connect!

