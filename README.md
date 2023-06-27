# CS130
## 4/3/2023 Week 1 Monday Lec 1
* Software engineering is about managing risk
* Timeline
* Student Development Environments
* learngitbranching.js.org
* Posted on CS130
## 4/5/2023 Week 1 Wednesday Lec 2
* Test it
* Types of tests
    * Unit, Integration, Regression
* Writing tests first
    * "Test-driven development"
    * API prototyping
        * Write unit tests that are examples of using your API
    * When you know the desired result before you know how to implement it
    * Before fixing a bug, write a unit test that fails because of the bug
* "Write more tests" isn't always the answer
    * Tests are expensive to write and maintain
* General guidelines
    * unit tests for use cases and common errors
* Testing case study: your project
* Config Parsing: Why is this separate from my server?
* Config Parsing API
* What to test?
* What to test? Apple SSL bug
* How to test?
    * Test units of code (classes, files, modules) in isolation
* Finding good test cases
    * make sure test cases test different, single thing
    * tests shouldn't depend on implementation
* Things that are hard to unit test
    * Global variables
    * Long, complex methods
    * Objects with state
    * Tight coupling (interdependent classes)
    * Bad abstractions
* How to unit test? GUnit
## 4/7/2023 Week 1 Friday Dis 1
* 1 assignment per week
    * individual, but others are other assignments
    * assignments due every tuesday, 12am
    * first two commits do not need reviews
* Review commits
* Git merge vs rebase
* git stash your changes to come back to work
    * git add -u
        * -u does not add new files
    * git commit --ammend
        * adds to the latest commit
    * git stash pop
* cherry picking
    * git cherry-pick commit-hash
* Unit, Integration, Regression, End-to-End, Performance testing
* Integration testing
    * Checking if the bigger system is working
* End-to-end testing
    * whole flow
* Performance testing
    * Threshold
    * P95, P99
        * P95, 95 requests are within one sec
* How many test cases do you need for a program?
    * Black box testing and white box testing
    * black box
        * treat code as a black box
        * see if it throws an error for some inputs
    * white box
        * have the source code
* Is it sufficient to check the output of the function?
    * No! states, performance, side-effects, etc. should be tested as well
* What test cases to choose?
    * Boundary cases, precondition and post-condition
* Unit Tests - Choosing Test Examples
    * Test code at its boundaries
    * Test pre and post conditions
* Assert fails if results aren't the same
* Expect generates a warning 
    * Used when you want to see all the errors
* Unit Tests
    * Test Coverage: choose a set of tests such that every line of program executes
    * Using pre-tested libraries/codes
    * Verify conservative properties
* Look at slides for the HW
## 4/10/2023 Week 2 Monday Lec 3
* Code reviews
    * Best proof of reusability is review
* Thinking system
    * Daniel Kahneman, Thinking, Fast and Slow
    * System 1
        * Intuitive, fast, but has higher error rates
    * System 2
        * Methodical, slow, low error rates, but is hard to engage
* Rubber duck debugging
    * Explain the problem to a rubber duck
* Research on code review
* Before sending code for review
* Mystery function
* Change descriptions
    * More than just what the change is
    * Why was the change made
    * How was the why accomplished
    * Any new testing
* During code review
    * Flag errors of execution
        * Unclear documentation
        * Typos
        * Style violations
        * Bad/missing tests
        * Tests
    * Apply deliberative thinking to find errors
    * Develop shared understanding about the purpose of the code
    * Establish N+1 availability on understanding of the code
        * Minibus
            * number of people could remove and still function
* Methods of code review
* Final Guidelines
* git head -~ for squashing commits
* Sample Code Reviews
* Public code review
* Webserver Development
* HTTP in (some) context
    * Status Cats
* Things you will see
    * MIME types
    * Header lines
    * \r\n\r\n (or \n\n)
    * Connection management
    * Error codes
    * Probers
* Command-line HTTP tools
* Write Logs
## 4/12/2023 Week 2 Wednesday Lec 4
* Blockers
* Other things
    * Ask questions effectively
* Assignment 2: In progress
* Knowledge you will need
    * Git + Gerrit
    * Boost Library
    * HTTP
    * Docker
    * Google Cloud Web + SDK
* Build Primer
* Quick vocab
    * "Build"
    * "Deploy"
* One step up
* Laptop different compilers
* Lesson 1
* Lesson 2
    * Builds should be repeatable
* Lesson 3
    * Remember: Valuable things go in revision control
* But.. consider different tool: make
* Building the config parser
* Exposing intermediates in g++
* Compilation
* Linking
* A dependency graph
* We can re-use intermediates
* Config parser Makefile, version 1
* Config parser Makefile, version 2
* Who makes the Makefiles?
    * Makefiles can get real complex, real fast
    * Solution: Generate makefiles
* GNU Build System
    * Autoconf + Automake
    * Notabile files:
        * Makefile.am
        * configure
        * Makefile.in
        * config.h
* CMake
    * Single tool
    * Notable files
        * CMakeLists.txt
        * build/
        * A ton of generated files
    * Run:
        * cd build
        * cmake ..
        * make
* CMake examples
    * Define library
    * Define executable
    * Add GTest tests
    * When run make test, it runs this as well
* Build system wishlist
    * some desirable features are contradictory
* Wishlist: Correct
    * Easy to happen in GNU Make where doesn't recognize changes
* Wishlist: Hermetic
* Wishlist: Flexible
    * Support other languages
* Wishlist: Easy to use
    * Build in one setup
    * Easy to set up for your project
* Wishlist: Automatable
* Wishlist: Fast
* Wishlist: Manage dependencies
* Wishlist: Manages dependencies automatically
* Wishlist: Integrated
* Wishlist: Scalable
* Building at scale
* Scale and change rate at Google
* Build scalability the typical way
* Google's solution
* What is deployment?
* ... fill in rest
## 4/14/2023 Week 2 Friday Dis 2
* Agenda
* Logistics
* Code Reviews
    * Why, What, How
    * Linters
* Why do we need code reviews
* What to look for during reviews
    * Are there any anti-patterns (god functions, very large functions)
    * Familiarity with code design patterns
* How to do code reviews
    * Pointers for reviewees
    * Send progress out early
    * Changes should be small for each review
* CMAKE
    * Cross Platform Development
* Docker
    * What are containers
    * Recap of Docker Terminology
    * Volume vs Bind Mount
    * Hypervisor
* Dockerfile
    * A textfile containing steps on how to build a particular image
* Boost.Asio
    * Boost
    * Focus - Boost.asio
* Docker container every time I make a change do I have to restart the container
* Boost.Asio - Basics
* Google Cloud Platform
* Assignment 2 Tips
* Assignment 2 Overview
* HTTP 1.1 Grammar
* Creating an echoing Web Server A Sample Workflow
* Testing a Web Server
* Updating Dockerfile
* Deploying to Google Cloud
## 4/17/2023 Week 3 Monday Lec 5
* A Note About Merging
* Know what you are merging
* Testing a web server
* But, you want it to be repeatable
* Author: I tested it and it works
* Bad practices
* Be sure to test the right things
* Testing boundaries
* Testing over the network?
* Factoring out a handler
* Testing your actual functionality
* More Testable Functionality
* Recap: Code structure before refactor
* Refactoring
    * Martin Fowler Refactoring Improving the Design of Existing code
    * Good tests will test the interface, not the implementation
* Refactoring Examples
    * Magic Number
        * kSecondsPerDay
    * Factory Method
    * Introduce Expression Builder
        * Java llamabock
    * Does parameter object require heap???
* Refactoring & Testing Recap
* Dependency Injection - Basics
* More refactoring patterns
    * Favor composition over polymorphism
* new considered harmful
* Dependency Injection
* Dependency Injection - From first principles
* Monte Carlo Simulations
* ASK WHY DOES DOCKER CONTAINER NOT SEEM TO BE RUNNING????
## 4/19/2023 Week 3 Wednesday Lec 6
* DI Frameworks, Testing State vs Interaction, Debugging, Integration Tests
* Assignment 2
* Dependency Injection Frameworks
* Dependency Injection
* Dependency Injection: Practical Application
* Dependency Injection: Implementation
* Dependency Injection: Use a Framework
* One weird thing
* One weird thing... How are connection ids generated?
* Testing
* Testing : Webdriver Torso
* Mocks vs Fakes
* Disclaimer
* Test Objects: Mocks, Fakes, etc..
    * Fake object
    * Mock object
* Testing state vs testing interaction
* Testing readability
    * DRY
    * DAMP
* Integration tests
* Integration tests: Web Driver
* Integration tests: Replay
* Integration tests: Screenshot
* What about web servers
* Simple web server integration test
* Debugging: Access Logging
* Debugging: Verbose Logging
* Debugging: Logging Libraries
* Debugging: Status Pages
* Debugging: Operating tracking + logging
* Continuous Build (CI)
* Continuous Build Example
* ASK IF IT MATTERS IF REPO HAS UPPERCASE LETTERS IN IT.
## 4/21/2023 Week 3 Friday Dis 3
* Agenda
* Why do we need to measure test-coverage?
    * Problem 1: Knowing if there are not enough tests for software
    * Problem 2: Might have too many redundant tests => causing quality assurance overhead
    * Problem 3: During software evolution, can't retest all tests again. Thus, we need to select a subset of tests to run
    * Problem 4: Need a way to tell how much testing is needed and where to focus
* Control Flow Graphs
* Measures of Coverage
* Analysis Steps: Draw CFG -> Complete Coverage Table
* Do the coverage tests
* Our Goal: >= 80% statement coverage
* Refactoring
* Martin Fowler's Refactoring Operations
* Builder Design Pattern
* Dependency Inversion Principle (DIP)
    * Question: If I have a LL class, how do I add a new node to it if I can't use new????
* Is this code violating DIP?
* Test Doubles: Mocks, Stubs, & Fakes
    * All three used in Unit Testing, replace class dependencies
    * Allow isolation of class under test
    * Lots of similarities, lets review the main differences
* Fakes
    * Objects that have working implementations, but not same as production once. Usually they take some shortcut and have simplified version of production code
* Fake Examples
* Stubs
    * objects that hold predefined data and uses it to answer calls during tests
* Stub Example
* Mocks
    * Mock are objects that registers calls they recieve
* They are: Test Doubles
* Where to use mocks?
    * Anything non-deterministic that can't be reliably controlled within the unit test
* GMock example - coin flipper
* Google Mocks to the Rescue!
* GMocks: Setting Expectations
* Combining GMocks with GTest
* Assignment 3 - Workflow and Tips
* Question about continuous build????
* Question about base.Dockerfile??? Multi-build steps???
* Integration Test
    * Testing binaries
    * Instead of port you have a config file
## 4/24/2023 Week 4 Monday Lec 7
* Static + Runtime Analysis
* Assignment reminders
    * Use same note sheet for all assignments
    * TL should NOT be submitting any changes
    * Project health is important
        * Each CL should do one thing
        * Criteria for coverage
            * Line coverage is really important
* Goals of this lecture
    * Explain static and runtime analysis
    * Discuss the pros and cons of the various approaches
    * Show you how to use such analysis in your applications
* Static analysis
    * Compiler warnings (i.e. -Wall)
    * Type checking in the compiler
    * Linters
* Compiler warnings
    * First of all you should use -Wall to enable lots of warnings and use -Werror to turn them into errors
* Static type checking
    * Static type checking gives you compile time errors about illegal operations
* Linters
    * Lint was a tool originally developed alongside the C programming lanaguage
    * It was originally intended to help catch nonportable constructs
    * Often, you'll find a less pedantic linter built into compiler frontends
    * Linters may not seem like static analysis
    * But they correct more than style
    * Many errors manifest as simple typos that are allowed by the compiler but are likely semantically wrong
* What is static analysis?
* Example: Use after free
* Example: Buffer Overrun
    * Reading or writing past
* An aside: How are Buffer Overruns Exploited?
* Example: Deadlock Detection
* An aside: Lock Annotation
    * template metaprogramming
    * macros are all CAPS
        * replaces verbatim with other thing
* Example: Uninitialized variable
* Aside: Type checking printf()
* Example: Dead code
    * It is possible to prove that certain blocks are never reachable
* How static analysis works
* Abstract Interpretation
    * Walk the control flow graph
    * Keep track of things that are true when a given unit of code executes
    * Determine if invariants are broken
* Data Flow Analysis
    * Keep track of the set of possible values a variable can take at a given point in the program
* Limitations of static analysis
    * these are an exponential number of paths through a program
* Static Analysis: Overcoming limitations
    * balance between low recall and low precision
* Static Analysis: Overcoming limitations
    * Another example: Typescript
    * Tool to perform static analysis, tool to auotmatically generate Javascript form Typescript
        * The Typescript compiler
* clang-format
    * Uses LLVM's abstract syntax tree
    * Allows automated reformatting of large swaths of code quickly and configurably
    * Works with lot of languages
    * WHAT IS UNICODE???
* Runtime analysis
    * Alternatively, you could just run the program in an instrumented runtime
    * Then just inspect what happened
    * Think of your brute force debugging sessions where you add printf()s until you find the issue
* How runtime analysis works
    * Just a virtual machine that is checking for bad states (e.g., SIGSEGV, deadlock, etc.)
    * Can keep track of real in-progress state, and pinpoint issues
* Limitations of runtime analysis
    * In some cases, hardware acceleration is available
    * For example, x86 has support for setting a breakpoint when a particular memory address is written to
    * This has virtually no impact on program execution speed
* Available runtime analysis tools
    * gcov, asan, tsan, gdb, valgrind, memcheck
* Demo of gcovr, lcov
    * g++ -o main -fprofile-arcs -ftest-coverage main.cc
* Demo Video of gdb + Valgrind
* Static Analysis vs Runtime Analysis
## 4/26/2023 Week 4 Wednesday Lec 8
* Assignment 4
* Notes: Source repos
    * One repo going forward
    * Only add source code
* Notes: Testing
    * Unit tests
        * Should they bind to a network interface + port?
            * No
        * Shouldn't just test if your source code changed
            * What does this mean???
    * Integration tests
        * Should start server, kill server
        * How to not bind to a port in use?
        * netstat
            * see if a port exists
            * lsof
* Notes: Development
    * Build in development environment, run in development environment
        * Expose ports with start.sh
    * Docker useful for testing deployment
    * DNS submdomains
        * www -> 127.0.0.1 placeholder
    * Use tags to mark images to be used for grading
        * :assignX
* Logging
* Important questions
* Why log?
    * Take a guess
    * Development, Debugging, Security, Monitoring, Usage insights
    * Boost.log, C++ string streams, Severity, Message
* When to log?
    * Every time interesting things happens 
    * Ready to serve
    * Serving a request
    * Errors
    * Shutting down
* What to log?
    * Basic purpose of web server logs:
        * Verify correct usage
        * Detect abuse
    * But what specific info? No answers wrong!
    * Timestamp, Thread ID, IP of request, Severity, ... and more
* Where to log?
    * Goals for statement logs
        * Inspect manually, parse with tools, do not fill disk, persist after restart or crash, resilient to hardware failures
    * Log sinks
        * Console stdout / stderr, File(s) on disk, Remote server
* Status pages (human readable)
* Status pages (machine readable)
    * Useful for monitoring (assignment 8)
* Notes on severity
    * Usually multi-level
        * trace/verbose/debug, info, warning, error
    * Specify minimum severity level for log destinations
        * logLevel=info includes info,warning, and eror
* Logging to disk
    * How do you avoid filling up the disk?
* Logs on Docker vs Logs on Google Cloud
* Logging vs Privacy
* Be careful what you log
    * Google Steet View cars
* There are laws now
    * Obtain consent, report data breaches, allow takeout, right to be forgotten, design with privacy
* Privacy challenges
    * Must delete all data N days after a user deletes their account
    * Hard analytics questions:
        * How many visits did we see last year
        * How many unique visitors did we see last year?
* Solutions: Aggregation
    * Aggregated data is generally not personally identifiable
    * Derived counts and stats are OK to keep indefinitely
* Solutions: Pseudononymization
    * Hash the PII and store the hash to count uniques
    * HMAC-SHA2 hashes are hard to reverse
    * Real anonymization is hard
* Privacy in practice
    * Privacy needs to be a first-class concern
    * Privacy needs to be considered early
    * Privacy and security go hand in hand
    * Data access controls are critical
        * We can't read your gmail
* Error Handling and Recording Information
* You thought you were finished?
    * Things working is just the first step
    * Now for lots of thinking about every possible error condition
    * The good news: your code is working, much easier to add code now
* Example 1
    * LOG(FATAL) logs message and exits server
        * best time to crash is at beginning of program
* Example 2: How about this?
    * Fail the server without a port number
* Example 3: This?
    * logging calculations every iteration
* Example 4: How about this?
    * Log when finished setups
* Error handling strategies
    * Crashing, returning faillure responses from requests, recovering from errors, recording info
    * When it is good to crash, good to surface errors to users, good to hide errors from users
* When to crash/fail
    * Crash? seriously?
    * Can you fail just one
* Aside: how to handle errors
    * Many different strategies
        * Boolean success return value
        * Error codes
        * Exceptions
        * "Global" (thread local) erno variable (not recommended)
        * "StatusOr"
    * "Translate" the error on the way up
    * What should the user see?
* The difficulties of recovering from errors
    * Recovery
        * Seems like a good idea, but is it worth the effort
        * Requires careful design
* Midterm Preview
* Impact
* Scope
    * Lectures 1-8
    * Assignments 1-4
* Format
    * 1 hour
    * short answers
## 4/28/2023 Week 4 Friday Dis 4
* About Midterm
    * Range: Lec 1-8, Hw 1-4
* Static Analysis
    * Type Checking, Type Inference, Linting, Compiler Warnings
* Type Checking
    * Type Error
        * undesirable program behaviour caused by a discrepancy between differing data types for the program's constants, variables, and functions
    * Static Type Checking
    * Dyanmic Type Checking
* Type Checking
    * Strongly Typed Languages
    * Weakly Typed Languages
* Strongly Typed LAnguages
    * Use of programming 
* Type Inference
    * Type Inference is the automatic detection of the data type of an expression
* Linters
    * A Linter is a tool
* Compiler Warnings & Errors
    * Finding all possible run-time warnings
    * Use after free
    * Buffer overrun
    * Deadlock detection
    * Uninitialized variable
    * Dead code
* How does Static Analysis work
    * Abstract interpretation
    * Data Flow Analysis
    * Symbolic Execution
    * Hoare Logic
* Finding infeasible path through symbolic execution
* Logging
    * Why do we need logging?
    * Makes troubleshooting and debugging of software more manageable
    * Provides a way to monitor real world applications
    * Security
    * Compliance and audit
* What information to log
    * NCSA Common log format
        * A fixed log format is used by web sevres when they generate server log files
        * Format
        * Ex
        * Is the Host the ip address of the user visiting???? Also auth-user is the user?
* Boost.Log
    * Initialize logging to a file
    * Create a log file named log0.log and add messages with greater severity
* Assignment 4 - Logging
    * Be sure to include other request info
    * Assignment 4 - Static Web Server
* Assignment 4 - Static Web server
    * MIME
    * What is the viewer application in the MIKE type????
* Midterm Sample Questions
    * Sample Question 1
        * git add ., git commit, git review
        * git pull, git rebase 
    * Sample Question 2
    * Sample Question 3
    * Sample Question 4
* Other possibilities (include but not limited to)
    * E.g. motivations of code review/testing
    * What log level to use
    * E.g. Static and runtime analysis?
* CHECK WHEN THE HTTP REQUEST IS INVALID
## 5/1/2023 Week 5 Monday Lec 9
* API Design
* Webserver Architecture
* Web Server Components
* Request Handlers
* Request Container and Parser
* Response Container and Generator
* Mime Type Resolution
* Other Web Server Components
* API Design
* What is an API?
* API Design
* Properties of Good API Design
* Properties of Bad API Design
* API Hall of Shame
* API Lifecycle
* Corollaries of the API Lifecycle
* Design Patterns
* Design Patterns: An Observation
* Design Patterns: Observer
* Design PAtterns: Lazy Initialization
* Design Patterns: Factories
* Design Patterns: Singleton
* Design Patterns: Pools/Freelists
* Design Patterns: RAII
* Design Patterns: Decorators
* Design Pattern: Continuation
* Design Patterns: Strategy
* Antipatterns
* Antipattern: Stringly typed
* Antipattern: Unclear Object Lifetime
* API Example
* CSV Parser Interface Critique
## 5/8/2023 Week 6 Monday Lec 10
* Mid-quarter update
* CS130 Goal
    * Code reviews, Testing, Revision Control, Teamwork, Tools, like coverage and static analysis
* Anti-patterns
* Expectations reminder
* Outline
* Config file format
* Warm-up: comments
    * we use hashtag
    * strings constant is not internal
* Specifying locations
* Handler arguments
* Misc
    * Optional slash at the end
* Request Handlers
* Handler Instantiation
    * What is REGISTER_HANDLER(Echo) = Registry::RegisterHandler(Echo::kName, Echo::Init)
* Handler configuration
* Dispatching
## 5/10/2023 Week 6 Wednesday Lec 11
* The Art of Readable Code
* Outline
* Code readability
* Many code quality mantras
* Fundamental Theorem
* Code length
* Code size
* Function length
* Naming
* Other "units"
* Use the type-system
* Obscure name vs Clear name
* Embedded Logic
* Commenting
* What to Comment
    * Code self documenting
* Be Concise
* Be Robust
* Comparison Expressions
    * LHS more in flux, RHS more constant
* Unnecessary variables
* Avoiding Complexity
    * Range overlap: re-approach
        * Check if two ranges don't overlap
* Avoid Nesting
## 5/12/2023 Week 6 Friday Dis 6
* Singleton
* Factory Method
* Adapter
    * Definition: The Adapter Pattern allows objects with incompatible interfaces to collaborate
* Adapter: a.k.a. Wrapper
* Strategy Design Pattern
* Strategy Design Pattern - Example
* Template Design Pattern
* Observer Design Pattern
* Readable Code
    * Code length
    * Comparison LHS in flux
* Conflict Resolution
* QUESTION: Should we include functions like debugging helpers in CLs???
    * ALSO why use C++?
    * Can you just do the research on the LLM on your own? (Can you publish outside school, why not list professor)
## 5/15/2023 Week 7 Monday Lec 12
* Midterm
* Code Review: CL description
* Major pieces / what you can reuse
    * Don't write to fs for unit tests
* Possible workflows
* Concurrency
* Background
    * Threads, processes
    * Mutexes, sempahores
    * Critical sections, race conditions, etc.
* Shared Memory
* Why Concurrency?
* Concurrency is hard
* Googlers do it wrong
* What's the problem
* Strategy 1: Be Slow
    * Lesson: Always profile before you optimize
* Strategy 2: Isolate
    * Example 1: An operating system
    * Example 2: A web indexer
    * Example 3: A web server
* Strategy 3: Use a Library
* Threads in C++11
* Time for a design review
* An actual design discussion
* Threads in C++11: Passing Data
* Threads in C++11: Returning values
* Strategy 4: Use a mutex
* Strategy 5: Never forget to unlock
* Strategy 6:
* Strategy 7:
## 5/17/2023 Week 7 Wednesday Lec 13
* Building Supercomputers
* Web servers in 2000
* Drawbacks of big iron
* Datacenter Efficiency
* Distributed Applications
* Performance critical for load balancing
* Example: MapReduce
* Example: Bigtable (data model)
* Example: Bigtable (system layout)
* Example: Bigtable (application flow)
* Example: Spanner (logical data model)
* Example: Spanner (physical data model)
* Example: Spanner (replication)
* Example: Spanner (external consistency)
* Example: Spanner (transaction protocol)
* Distributed System Design Patterns
* Manager / worker
* Dynamic (load-based) sharding
* Separate routing path from data path
* Admission control
* Distributed consensus
* Decoupling through queuing
* Memcache
* MVCC: Multiversion concurrency control
* Bad: Storing metadata in the system itself
* Bad: Synchronous global config rollout
* Known Hard Problems
* CAP theorem
* Commits across atomicity domains
* Balancing QoS and utilization
* Rollouts and protocol upgrades
* Reprocessing
* Data Moves
## 5/19/2023 Week 7 Friday Dis 7
* Agenda
* Concurrency
* Threads vs Processes
* MapReduce
    * Software Framework
* MapReduce - Example
* Sharding
* Types of Sharding
* Distributed Consensus: RAFT
* Consensus Algorithm: RAFT
* CAP Theorem
* Zero Down Deployment
* Assignment 7 Tips
## 5/22/2023 Week 8 Monday Lec 14
* Performance
* Sufficiently unit testing
    * Write tests
* About those distributed systems
* Youtube goes down too
* We ported an existing code base
* Old code
* New code
* Before you start optimizing: when is it fast enough?
* How do we keep it fast?
* Performance monitoring
* Reproducibility is a huge problem
* UIs are a different kind of distributed system
* Gather information from the "wild" (Remote profiling)
* Pretend to be fast
* No. Make the code lazy
* Facebook's loading shims
* Capacity Planning
* Capacity Planning -- Automation
* Load testing case study
* Common Failure Modes of Distributed Systems
* Producer-consumer rate mismatch
* Hotspots
* Death ray
* Amplified rare events
* Debugging Distributed Systems
* Status PAges
* Logging
* Local Request Tracing
* Distributed Tracing
* DOES IT MAKE SENSE TO MAKE A UTILITY FUNCTIONS FILE WITH A BUNCH OF USEFUL FILES TO HAVE
## 5/24/2023 Week 8 Wednesday Lec 15
* Persistent disks
* Project choice
    * Use CRUD?
    * Use your own CRUD?
* Monitoring overview
* Site Reliability Engineering Book How Google Runs Production Systems
    * Jennifer Petoff
* Pryamids 101
    * Maslow's Hierarchy of Needs
    * Self-actualization is the goal
    * Physiological needs must be met
* Pyramids 101
    * John Wooden's Pyramid of Success
    * Competitve Greatness is the goal
    * Foundations are most important
* Pyramids 101
* Production Terminology
* Monitoring Overview
* Time Series
* Black-box monitoring
* White-box monitoring
* Implementing Server Monitoring
* Exposing Server Data
* Viewing Server Data
* Integration with monitoring
* Using Monitoring: Dashboards
* Other parts of the monitoring service
* Client Interface
* Using Monitoring: Responses
* Incident Response
* Alerts
* Alert severities
* Service Level Objectives (SLO)
* Implications of a strict SLO
* Minimizing downtime
* What causes downtime?
* SLOs are a risk budget
* SLOs affect development practices and priorities
* Minimizing toil
* Documentation
* Starting on a new project
* Product requirements documents (PRD)
* Technical design docs
* DNS Prefecting
* Good requirements are...
* Technical design docs: extra credit
* API docs
* JavaDoc
* "The source code is the documentation"
* Use Cases
    * Tab to Search
* And more...
    * User stories
    * UI mocks
    * Tutorials
    * End-user documentation 
    * Contributor docs (how to be a team member)
    * FAQs
* Even cartoons
## 5/26/2023 Week 8 Friday Dis 8
* Opportunities for Web Server Performance Improvement
* QoS vs QoE
* Monitoring
* Invariant Testing
* Loop Invariants
## 5/31/2023 Week 9 Monday Lec 16
* Postmortems
* A long ago outage
* Dissecting a recent postmortem
* Summary
* Impact
* Even more impact
* Root cause
* Timeline
* Analysis
* Action items
* What is not in this postmortem?
* Bringing it all together (on final)
* Things were always broken
* Consider the cost of prevention
* Small, informal postmortems
* Asking others for postmortems
* Retrospectives
* Team Structure
* Q&A with Ben Collins-Sussman
* Almost certain to be on your team
* Likely to be on your team
* Sometimes on your team
* Occassionaly on or near your team
* The business
* Human resources
* Levels (from low to high)
* Prevailing development philosophies
* Bonus: Negotiation Crash Course
* File structure?? PhD?? Using code from JSON??
## 6/2/2023 Week 9 Friday Dis 9
* Agenda
* JavaDoc Style Documentation
* PostMortem
* Example Study - GCP Outage Postmortem
* Requirements Analysis
* Good Requirements
* Requirements Analyses with Unified Modeling Language (UML)
* Requirements Analysis with UML
* UML Diagrams: Use Case Diagrams
* More components of Use-Case Diagrams
* Use Case Diagram Example
* Requirements Analysis with UML
* UML Diagrams: Activity Diagrams
* Activity Diagrams
* Use Case Slicing
* Frame Operators
* UML Diagrams: Sequence Diagrams
* Example: Distribution System
* Complete this Sequence Diagram of the Order Totalling functionality
* Step 4 - States of Complex Objects
* UML Diagrams: State Machine Diagrams
* State Machine for Checkout functionality
* Requirements Analysis with UML
* UML Diagrams: Class Diagrams
* UML Diagrams: Class Diagrams - Relationship
* Iterative Modeling
## 6/5/2023 Week 10 Monday Lec 17
* Deployments, Experiments, and Launches
* Central topic for today's lecture: New Functionality
* Deployments
* Safety in numbers
* Staging
* What is MemCache?
* Develop
* Wire formats
* "No downtime"
* One solution: Protocol Buffer
* Backwards compatibility
* Forwards compatibility
* Key Problems to Solve
* Feature Flags
* Experiments
* Experiment Setup
* Experiment diversion
* Counterfactuals
* Unintentional Design
* Self Design
* "Expert" Design
* Activity Oriented
* Emotionally Oriented
* System bible book read