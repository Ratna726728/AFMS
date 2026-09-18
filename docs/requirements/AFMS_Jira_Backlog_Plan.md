Application Form Management System (AFMS)
Jira Epic, Story & Sub-task Backlog — Initial Project Plan
Purpose: A ready-to-use Jira backlog for building the AFMS CLI application from scratch. Ubuntu is used throughout DEV, QA and PROD. The application uses Java, JDBC and MySQL, while Vagrant/VirtualBox provide the environments and Git/GitHub provide source-control history.
1. Project Overview
AFMS is a command-line application that collects application-form data from a user and stores/retrieves it from MySQL through Java and JDBC. Three isolated environments will be maintained: DEV for development, QA for testing, and PROD for production-ready releases.
2. Technology Stack
•	Java
•	MySQL
•	JDBC
•	Ubuntu
•	Vagrant
•	Oracle VirtualBox
•	Git Bash
•	Git
•	GitHub
•	Jira
3. Environment Plan
Environment	Purpose	OS	Example IP
DEV	New development and developer verification	Ubuntu	192.168.56.10
QA	Testing and validation	Ubuntu	192.168.56.11
PROD	Production-ready application	Ubuntu	192.168.56.12
Example IPs are placeholders. Record the final Ubuntu release, box version, VM resources, hostnames and IPs in Jira when implementation starts.
4. Jira Hierarchy
•	Epic — major project area or milestone.
•	Story — meaningful deliverable within an Epic.
•	Task — technical work required to complete a Story.
•	Sub-task — small executable step under a Story/Task.
•	Bug — defect found during development or QA.
5. Epic List
Epic ID	Epic Name	Scope
EPIC-01	Project Planning & Documentation	Requirements, scope, architecture and documentation.
EPIC-02	Host & Infrastructure Setup	Git Bash, VirtualBox, Vagrant, networking and shared-folder design.
EPIC-03	Ubuntu Environment Provisioning	DEV, QA and PROD Ubuntu virtual machines.
EPIC-04	Development Tools & Java Setup	Java and CLI development prerequisites.
EPIC-05	MySQL Database	MySQL installation, schema, users, permissions and data design.
EPIC-06	JDBC Data Access Layer	JDBC configuration, connections and database operations.
EPIC-07	CLI Application & Form	CLI menus, form input, validation, persistence and retrieval.
EPIC-08	Git & GitHub Workflow	Repository, branching, commits, pull requests and traceability.
EPIC-09	QA & Testing	Test strategy, test cases, QA environment and defects.
EPIC-10	Deployment & Release	DEV → QA → PROD promotion, deployment, verification and rollback.
EPIC-11	Operations & Troubleshooting	Logs, backups, diagnostics and operational runbooks.
6. Detailed Story & Sub-task Backlog
Epic	Issue	Story	Topics / Sub-tasks
EPIC-01	AFMS-01	Define project scope and requirements	• Document application purpose and CLI-only scope
• Define functional requirements
• Define non-functional requirements
• Define environment requirements
• Document technology stack and constraints
• Review and baseline requirements
EPIC-01	AFMS-02	Create application architecture documentation	• Define high-level architecture
• Define application/data flow
• Define DEV/QA/PROD flow
• Create architecture diagram
• Document architecture decisions
EPIC-01	AFMS-03	Create project documentation structure	• Create docs directory structure
• Create README outline
• Create environment documentation template
• Create database documentation template
• Create development/testing/deployment templates
EPIC-02	AFMS-04	Prepare host development tools	• Verify Git Bash
• Verify Git
• Install/verify Oracle VirtualBox
• Install/verify Vagrant
• Record versions
• Document host setup
EPIC-02	AFMS-05	Create Vagrant project structure	• Create project directory
• Create Vagrantfile
• Define VM naming convention
• Define private network
• Define shared folder
• Document Vagrant configuration
EPIC-02	AFMS-06	Design VM networking and shared-folder strategy	• Define DEV/QA/PROD hostnames
• Define static IP scheme
• Verify VM connectivity requirements
• Define shared-folder mount point
• Document isolation rules
EPIC-03	AFMS-07	Provision Ubuntu DEV VM	• Select Ubuntu box
• Configure VM name
• Configure CPU/RAM/disk
• Configure network/IP
• Configure shared folder
• Boot VM
• Verify SSH/hostname/IP
• Document DEV build
EPIC-03	AFMS-08	Provision Ubuntu QA VM	• Select Ubuntu box
• Configure VM name
• Configure network/IP
• Configure shared folder
• Boot VM
• Verify SSH/hostname/IP
• Document QA build
EPIC-03	AFMS-09	Provision Ubuntu PROD VM	• Select Ubuntu box
• Configure VM name
• Configure network/IP
• Configure shared folder
• Boot VM
• Verify SSH/hostname/IP
• Document PROD build
EPIC-03	AFMS-10	Standardize Ubuntu base configuration	• Update package metadata
• Install common CLI utilities
• Configure hostname
• Verify network/DNS
• Document base configuration
EPIC-04	AFMS-11	Install and verify Java on DEV	• Select Java version
• Install JDK
• Set JAVA_HOME if required
• Verify java version
• Verify javac version
• Document installation
EPIC-04	AFMS-12	Prepare Java CLI project	• Create Java source structure
• Create package naming convention
• Create application entry point
• Run initial CLI application
• Document build/run commands
EPIC-04	AFMS-13	Configure development tooling	• Verify required CLI tools
• Configure Git identity
• Define coding conventions
• Define configuration approach
• Document developer setup
EPIC-05	AFMS-14	Install and configure MySQL on DEV	• Install MySQL server/client
• Enable/start service
• Verify service status
• Secure installation
• Test local login
• Document installation
EPIC-05	AFMS-15	Design AFMS database schema	• Define database name
• Define applications table
• Define columns/data types
• Define primary key
• Define timestamps
• Define constraints
• Review schema
EPIC-05	AFMS-16	Create database schema scripts	• Create schema SQL
• Create seed/test data SQL if required
• Test scripts on DEV
• Document execution order
EPIC-05	AFMS-17	Create application database user	• Create non-root application user
• Grant minimum privileges
• Test permissions
• Document credential handling
EPIC-06	AFMS-18	Configure MySQL JDBC dependency	• Select Connector/J version
• Add dependency
• Verify dependency resolution
• Document dependency
EPIC-06	AFMS-19	Implement JDBC connection management	• Create DB configuration
• Implement connection utility
• Handle connection errors
• Test connection
• Document configuration
EPIC-06	AFMS-20	Implement application data access	• Create model/entity
• Create DAO/repository structure
• Implement insert
• Implement select
• Implement update if required
• Implement delete if required
• Use PreparedStatement
EPIC-07	AFMS-21	Design CLI application flow	• Define startup flow
• Define menu/options
• Define form prompts
• Define success/error messages
• Document user journey
EPIC-07	AFMS-22	Implement application-form input	• Implement first-name input
• Implement last-name input
• Implement email input
• Implement phone input
• Implement address/location input
• Implement other agreed fields
EPIC-07	AFMS-23	Implement input validation	• Required-field validation
• Email validation
• Phone validation
• Length/range validation
• Invalid-input retry flow
• Document validation rules
EPIC-07	AFMS-24	Persist application through JDBC	• Collect validated data
• Map data to model
• Call DAO
• Insert into MySQL
• Confirm persistence
• Handle database errors
EPIC-07	AFMS-25	Implement application retrieval	• Define retrieval command/menu
• Query database
• Map ResultSet
• Display application details
• Handle no-result case
EPIC-07	AFMS-26	Implement CLI error handling	• Handle invalid input
• Handle DB connection failure
• Handle SQL exceptions
• Provide user-safe messages
• Log technical details where appropriate
EPIC-08	AFMS-27	Create Git repository	• Initialize repository
• Create .gitignore
• Create initial README
• Create initial commit
• Verify history
EPIC-08	AFMS-28	Create GitHub repository and remote	• Create GitHub repository
• Configure remote
• Push initial branch
• Verify repository content
• Document repository setup
EPIC-08	AFMS-29	Define Git branching and commit strategy	• Define main branch
• Define development branch if used
• Define feature branch naming
• Define commit format
• Define pull-request workflow
EPIC-08	AFMS-30	Link Jira work with Git changes	• Use Jira issue keys in branch names
• Use Jira issue keys in commits
• Define PR convention
• Verify traceability
EPIC-09	AFMS-31	Create QA test strategy	• Define test scope
• Define functional categories
• Define negative tests
• Define database failure scenarios
• Define regression approach
EPIC-09	AFMS-32	Create application test cases	• Valid form submission
• Missing required field
• Invalid email
• Invalid phone
• Boundary values
• Database unavailable
• Constraint/duplicate scenario if applicable
• Retrieval with no records
EPIC-09	AFMS-33	Configure QA environment	• Install Java/runtime
• Install/configure MySQL
• Deploy test build
• Configure QA database
• Verify connectivity
• Document QA setup
EPIC-09	AFMS-34	Execute QA testing and defect workflow	• Execute test cases
• Record results
• Create Jira bugs
• Fix defects in DEV
• Retest in QA
• Perform regression testing
EPIC-10	AFMS-35	Define application deployment package	• Define build artifact
• Define configuration files
• Define deployment directory
• Define versioning scheme
• Document package contents
EPIC-10	AFMS-36	Deploy application to QA	• Prepare release
• Backup QA database if needed
• Deploy artifact
• Apply database changes
• Run application
• Verify smoke tests
• Record release
EPIC-10	AFMS-37	Prepare PROD environment	• Install runtime
• Install/configure MySQL
• Create PROD database/user
• Configure application settings
• Set permissions
• Document PROD setup
EPIC-10	AFMS-38	Deploy application to PROD	• Approve release
• Backup database
• Deploy artifact
• Apply schema changes safely
• Run smoke test
• Verify application
• Record deployment
EPIC-10	AFMS-39	Create rollback procedure	• Define application rollback
• Define database rollback strategy
• Test rollback
• Document recovery verification
EPIC-11	AFMS-40	Implement logging and operational checks	• Define log location
• Define log format
• Capture application errors
• Define startup checks
• Document log inspection commands
EPIC-11	AFMS-41	Create database backup and restore procedure	• Define backup command
• Plan backups if required
• Test restore
• Document retention
• Document recovery steps
EPIC-11	AFMS-42	Create troubleshooting runbook	• Application startup issues
• Java/JDBC issues
• MySQL issues
• Vagrant/VirtualBox issues
• Networking issues
• Shared-folder issues
• Common verification commands
EPIC-11	AFMS-43	Create final project documentation and handover	• Update README
• Update architecture
• Update environment docs
• Update database docs
• Update deployment guide
• Update troubleshooting guide
• Create final project checklist
7. Recommended Jira Creation Order
1.	Create the Jira project with key AFMS.
2.	Create all Epics from Section 5.
3.	Create the planning and infrastructure Stories first (AFMS-01 through AFMS-17).
4.	Create Git/GitHub Stories early (AFMS-27 through AFMS-30), before significant application coding.
5.	Create detailed Sub-tasks for the next work item rather than creating hundreds of tiny issues immediately.
6.	Use Jira issue keys in Git branch names and commit messages so work remains traceable.
7.	When an issue is completed, verify the work, update documentation, commit/push changes, and then move the Jira issue to Done.
8. Suggested First Sprint
•	AFMS-01 — Define project scope and requirements
•	AFMS-02 — Create application architecture documentation
•	AFMS-03 — Create project documentation structure
•	AFMS-04 — Prepare host development tools
•	AFMS-05 — Create Vagrant project structure
•	AFMS-06 — Design VM networking and shared-folder strategy
•	AFMS-07 — Provision Ubuntu DEV VM
•	AFMS-10 — Standardize Ubuntu base configuration
•	AFMS-27 — Create Git repository
•	AFMS-28 — Create GitHub repository and remote
9. Definition of Done
•	Implementation completed
•	Verification performed
•	Relevant documentation updated
•	Git commit created for code/configuration changes
•	GitHub push/PR completed when applicable
•	Jira issue updated with result/evidence
•	No unresolved blocker remains
10. Important Design Notes
•	Ubuntu is used for DEV, QA and PROD throughout the project.
•	The initial application is CLI-based; no web framework is required.
•	DEV, QA and PROD must have separate application/runtime and database state, even if the host uses one shared folder.
•	The Java application should use a dedicated MySQL account, not root.
•	JDBC database operations should use PreparedStatement and proper resource handling.
•	Secrets and passwords must never be committed to GitHub.
•	Exact Ubuntu box version, Java version, MySQL version, VM resources and IP addresses will be finalized during infrastructure tasks and recorded in Jira/documentation.

