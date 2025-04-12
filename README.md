
# Developer Testing Roadmap

![Roadmap](./developer-testing-roadmap.png)

## Test Concepts

- White Box
- Gray Box
- Black Box

## Test Design
- Criteria Base
    - Equivalence Partitioning
    - Boundary Value Analysis
    - State Transition Diagrams
    - Decision Table Testing
    - Graph Coverage
- Human Base

## [Naming Standards](https://dzone.com/articles/7-popular-unit-test-naming)
- MethodName_StateUnderTest_ExpectedBehavior
- MethodName_ExpectedBehavior_StateUnderTest
- test[Feature being tested]
- Feature to be tested
- Should_ExpectedBehavior_When_StateUnderTest
- When_StateUnderTest_Expect_ExpectedBehavior
- Given_Preconditions_When_StateUnderTest_Then_ExpectedBehavior

## Patterns

- [AAA Pattern](https://martinfowler.com/bliki/GivenWhenThen.html)
    - Arrange
    - Act
    - Assert
- [Four Phase Test](https://martinfowler.com/bliki/GivenWhenThen.html)
    - Setup
    - Exercise
    - Verify
    - Teardown

## Development approach
- TLD
- TDD
  - Read
  - Green
  - Refactor
- BDD
  - Gherkin
    - Given
    - When
    - Then
  - SpecFlow
  - Cucumber

## Test Types

- Functional
  - Unit Test
    - Terminologies
      - Isolated
      - Repeatable
    - Test Doubles
      - Dummy
      - Fake
        - AutoFixture
        - Bogus
      - Stub
      - Spy
      - Mock
        - Moq
        - RichardSzalay.MockHttp
        - NSubstitute
    - Internal Functions Testing
      - .NET Friend assemblies
    - Frameworks
      - XUnit
      - NUnit
  - Integration Test
    - Types
      - Non Incremental
        - Big Bang Integration
      - Incremental
        - Top - Down
        - Bottom - Up
    - Third party Integration
      - Database Sandbox
        - EFCore InMemoryDatabase
        - SQL Lite
      - Container Integration
        - .NET Test Container
        - Gitlab Service container
        - Github Service container
    - Mock Server
      - Mockit
      - Wire mock
    - Tools
      - White Box
        - .NET WebApplicationFactory
      - Black Box
        - Playwright
        - Postman
  - End-to-end
    - headless
    - headed
    - Tools
      - Playwright
      - .NET Web Application Factory
      - Cypress
      - Selenium
  - System Test
  - Acceptance Test
- Non-Functional
  - Performance Testing
    - Types
      - Load testing
      - Stress testing
      - Volume testing
      - Spike testing
      - Soak testing
    - Tools 
      - K6
      - Apache JMeter
  - Usability Testing
  - Compatibility Testing
  - Reliability testing
    - Failover
    - Fault tolerance
  - Architecture Testing
    - ArchUnitNET
- Other Test Types
- Smoke Testing
  - Smoke Testing
    - K8S readiness
    - K8S liveness
  - A/B Testing
  - Snapshot Testing
    - Verify
  - Canary Testing

## Test Pyramid

## Test Coverage
- CLI
  - dotnet-coverage
- Visual
  - IDE Tools
  - dotCover

## Test smells
- Test Logic
- Magic strings
- Slow Tests
- Multiple Act
- Stub static references
  - DateTime
  - System.IO
- Flaky
- Test Duplication in test levels

## Clean Test Code
- Test code is as important as production code
- Duplication is okay, if it improves readability
- Use the Rule of Three to decide to refactor
- Test one condition per test

## Test execution
- Manual
- Automate
  - Without Pipeline
    - Git Hooks
      - [Husky .NET](https://alirezanet.github.io/Husky.Net/)
      - [Husky](https://github.com/typicode/husky)
  - With Pipeline
    - CI
    - CD

## Static Code Analysis
- Plugin
  - [analysis-tools](https://analysis-tools.dev)
- External
  - Sonarqube
  - Veracode
  - OWASP Code Pulse

## Books
- The art of unit testing - Roy Osherov
- TDD by Example - Kent Beck
- XUnit Test Patterns by Gerard Meszaros

# 🧠 Stay curious!
