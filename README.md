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
