# Testing

JavaScript tests are usually run in the browser or on the frontend. Some JavaScript code is written for running a test for a page of the website or a single module of an application, and
then this code is combined with HTML as an inline event handler

### Types of Testing

  1. Unit Tests
  1. Integration Tests
  1. Acceptance Tests

#### [Unit Testing](https://github.com/harishv98/Testing/blob/master/QUnit%20testing%20methods/QUnit%20methods.md)

>Testing of individual functions or classes by supplying input and making sure the
output is as expected.

#### Integration Testing


>Testing combinations of units such as components and how they work together.
Individual software modules are combined and tested as a group.
It occurs after unit testing.

#### Acceptance testing

>Testing an application in the browser or on a device to analyze the performance
of the entire application also called as End-to-End testing.

### __Testing Software developement methods__

1. __TDD (Test Driven Development)__
    * The concept is that you write a test before you implement a function
    * It helps us to understand more about the function before implementation
1. __BDD (Behavior Driven Development)__
    * If you update the function, even without changing the inputs and outputs, 
    you must also update the test. This is a problem because it makes doing changes tedious
    * In BDD The test is thought as the first customer of the products and requires some 
     specifications in words of a human
    * You should not test implementation, but instead behavior

### __Types of testing Frameworks__

##### __Qunit__
1. Lots of support across the board
2. provides promise support
1. Lacks fluent syntax
1. Configuration is a headache, and must constantly be maintained
2. Require assertion libraries

##### __Jest__
1. Mock by default makes testing much simpler
2. Out of the box code coverage
3. Bundled with JSDOM to enable DOM testing
4. Fast
1. Mock by default screws up your classes, breaking tests
2. More dependencies and initial setup, e.g. we need to set up babel for transpiling the tests

##### __Mocha__
1. Simple setup
1. Headless running out of the box
1. Allows use of any assertion library that will throw exceptions on failure,   such as Chai
2. Highly extensible
1. Asynchronous testing is a breeze


