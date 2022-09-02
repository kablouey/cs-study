# Continuous Iintegration/Automated Building
## Part A: Review last week lecture  
### A. CI questions  
#### 1.  What are configuration management steps?  
##### Version Control:
- <span style="color:blue">Keep everything in version control</span>
- Check in regularly to Trunk
- Use meaningful commit messages
##### Managing dependencies:
- Managing external libraries
- Managing components
##### Managing Software Configuration
- Configuration and Flexibility
- Types of Configuration
- Managing Application Configuration
##### Manage Your Environment
- Tools to manage environments
- Managing the Change Process

#### 2. What are prerequisites for CI?
- Check-in regularly and consistently
- Create a comprehensive automated test suite
- Keep the build and test process short
- Use known environment, e.g. your machine

#### 3. What type of tests exist in software production?  
Tests can be described in a few ways:
- They can be <strong> automated</strong> or <strong>manual</strong>
- <strong>Business facing</strong> or <strong> Technology facing</strong>
- <strong>Support the programming</strong> or <strong>critique the project</strong>
![[Pasted image 20220818175944.png]]
We have:
- Functional acceptance testing
	- Should be written, and ideally asutomated before development on a user story starts
	- Tests functionality of the program, but non-functional also exists
- Unit testing:
	- Tests individual pieces of code in isolation
- Nonfunctional accpetance testing:
	- Tests non-functional aspects of the project, eg. capacity, availability, security, scalability
- Component/Integration tests:
	- Tests how larger sections of code interact. Larger and slower than functional tests
- Deployment tests:
	- Checks project is install correctly, configured correctly, able to contact services it requires and is responding
- Test doubles:
	- Creating dummy objects, stubs, spies, mocks. ie. Non-database entities to test object behaviour
	
#### 4. What is deployment pipeline?  
Deployment Pipeline is the route of all processes relating to the project.
It changes depending on project, software used, over time.
Eg. Delivery team, to version control, to uni testing, to acceptance testing, to release

Can be separated into the following:
1. Commit stage:
	- Technical level i.e. Cope compiles, passes a suite of (primarily unit-level) automated tests, and runs code analysis
2. Automatied Acceptance Tests stage:
	- Asserts the program works at the functional and non-functional level, behaviourly it meets the needs of the user/client specifications
3. Manual Test stage:
	- Asserts the system is usable and fulfills requirements.
	- May catch defects not caught by automated tests
	- Checks it provides value to its users
	- May include, exploratory testing, integration environment and UAT
4. Release stage:
	- Delivers the applicatoin to the users, whether it be a packaged application format or deploying into a production or stagin environment (staging being the same as production, but for testing)
 

### B. Automated Build Questions  
#### 1. Explain briefly what is build lifecycle?  
Build lifecycle includes the build process i.e.:
- Compile source code
- Copy resources
- Generate documentation
- Generate version number
- Generate installation program/manifest
- Compress/archive
As well as other build related processes:
- Running automated tests
- Uploading to distribution server
- Generating source code/bindings

Building requires configuration, depending on technology used, as well as the deployment environments. Eg. different builds for android and web.

Building is incremental. Each build involves changing/reperforming lifecycle processes.
Automation is key to making this a less painful process.
#### 2. How can you build incrementally?  
Building incrementally is possible through only needing to recompile the smallest amount of code possible. If we recompile the whole application for one specific segment of code, then that is wasted time for developers. Note: clean builds are important for distribution as builds can accumulate differences over time that require clearing 
#### 3. What’s Apache Ant?  
Apache Ant is a build management tool. That is, it automates the build process.
It is simple compared to newer build tools, but is the Java standard. Not a lifecycle tool/framework

It performs tasks according to a buildfile (build.xml) which determines the build process.

Commoinly defined targets:
- prepare
- build
- clean
- dist
- doc
- test
- run

#### 4. What is Apache Maven?  
A more sophisticated build tool. A lifecycle tool, and a framework.
A software project management and comprehension tool.
Project oriented.
Convention over configuration:
- Reuse
- Simplicity
- Less error-prone
- Facilitates communicatoin among teams
Dependency management within the pom.xml (Project Object Model) build file.
- Extensible
- Reusable through central repositories

#### 5. What is Maven lifecycle
1. generate sources
2. compile (compiler) || `mvn compile` 
3. test-compile (compiler)
4. test (surefire) || `mvn test`  
5. package || `mvn package` 
6. integration-test
7. verify
8. install (jar, install) || `mvn install` 
9. deploy || `mvn deploy` 

These are lifecycle plugins.

### C. Meet your tutor, show your backlog and if setup your backend basecode, please  show this with your tutor as well. Run a normal standup meeting with your tutor  and answer standup questions individually.