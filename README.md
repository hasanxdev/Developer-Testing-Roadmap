
# Developer Testing Roadmap

![Roadmap](./developer-testing-roadmap.png)

## Test Concepts
- White Box
- Gray Box
- Black Box

## Test Design
- [Criteria Base](https://www.testing101.net/post/top-10-test-design-techniques)
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
  - Tools
    - [Cucumber](https://cucumber.io/docs/installation)

## Test Types

- Functional
  - Unit Test
    - Terminologies
      - Isolated
      - Repeatable
    - [Test Doubles](https://martinfowler.com/bliki/TestDouble.html)
      - Dummy
      - Fake
      - Stub
      - Spy
      - Mock
    - Internal Functions Testing
      - [.NET Friend assemblies](https://learn.microsoft.com/en-us/dotnet/standard/assembly/friend)
    - Frameworks
      - [XUnit](https://xunit.net/)
      - [NUnit](https://nunit.org/)
    - Mock Tools
      - .NET
        - [Moq](https://github.com/devlooped/moq)
        - [RichardSzalay.MockHttp](https://github.com/richardszalay/mockhttp)
        - [NSubstitute](https://nsubstitute.github.io/)
      - JS
        - [Jest](https://jestjs.io/)
      - Python
        - [unittest.mock](https://docs.python.org/3/library/unittest.mock.html)
      - PHP
        - [PHPUnit Mock Objects](https://docs.phpunit.de/en/10.5/test-doubles.html)
  - Integration Test
    - [Types](https://www.geeksforgeeks.org/software-engineering-integration-testing/)
      - Non Incremental
        - Big Bang Integration
      - Incremental
        - Top - Down
        - Bottom - Up
    - Third party Integration
      - Database Sandbox
        - EFCore InMemoryDatabase
        - SQLite
      - Container Integration
        - .NET Test Container
        - [Gitlab Service container](https://docs.gitlab.com/ci/services/)
        - [Github Service container](https://docs.github.com/en/actions/use-cases-and-examples/using-containerized-services/about-service-containers)
    - Mock Server
      - [Mockito](https://site.mockito.org/)
      - [Wire mock](https://wiremock.org/)
    - Tools
      - White Box
        - [.NET WebApplicationFactory](https://learn.microsoft.com/en-us/aspnet/core/test/integration-tests)
      - Black Box
        - [Playwright](https://playwright.dev/)
        - Postman
  - End-to-end
    - headless
    - headed
    - Tools
      - [Playwright](https://playwright.dev/)
      - [.NET WebApplicationFactory](https://learn.microsoft.com/en-us/aspnet/core/test/integration-tests)
      - [Cypress](https://www.cypress.io/)
      - [Selenium](https://www.selenium.dev/)
  - [System Test](https://www.geeksforgeeks.org/system-testing/)
  - [Acceptance Test](https://www.geeksforgeeks.org/acceptance-testing-software-testing/)
- Non-Functional
  - Performance Testing
    - [Types](https://queue-it.com/blog/types-of-performance-testing/)
      - Load testing
      - Stress testing
      - Volume testing
      - Spike testing
      - Soak testing
    - Tools 
      - [K6](https://k6.io/)
      - [Apache JMeter](https://jmeter.apache.org/)
  - Usability Testing
  - Compatibility Testing
  - Reliability testing
    - Failover
    - Fault tolerance
  - Architecture Testing
    - .NET
      - [ArchUnitNET](https://github.com/TNG/ArchUnitNET)
    - PHP
      - [phpat](https://github.com/carlosas/phpat)
- Other Test Types
- Smoke Testing
  - Smoke Testing
    - K8S readiness
    - K8S liveness
  - A/B Testing
  - Snapshot Testing
    - .NET
      - [Verify](https://github.com/VerifyTests/Verify)
    - JS
      - [Jest](https://jestjs.io/docs/snapshot-testing)
    - Python
      - [snapshottest](https://github.com/syrusakbary/snapshottest)
    - PHP
      - [phpunit-snapshot-assertions](https://github.com/spatie/phpunit-snapshot-assertions)
  - Canary Testing

## Test Pyramid

## Test Data Generation
- .NET
  - [AutoFixture](https://github.com/AutoFixture/AutoFixture)
  - [Bogus](https://github.com/bchavez/Bogus)
- JS
  - [Faker.js](https://github.com/faker-js/faker)
- Python
  - [Faker](https://github.com/joke2k/faker)
- PHP
  - [FakerPHP](https://fakerphp.org/)


## Test Coverage
- CLI
  - [dotnet-coverage](https://learn.microsoft.com/en-us/dotnet/core/additional-tools/dotnet-coverage)
- Visual
  - IDE Tools
  - [dotCover](https://www.jetbrains.com/dotcover/)

## [Test smells](http://xunitpatterns.com/Test%20Smells.html)
- Test Logic
- Magic strings
- Slow Tests
- Multiple Act
- Stub static references
  - DateTime
  - System.IO
- Flaky
- Test Duplication in test levels

## [Clean Test Code](https://martinfowler.com/articles/practical-test-pyramid.html)
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
  - [Sonarqube](https://www.sonarsource.com/)
  - [VeraCode](https://www.veracode.com/)
  - [OWASP Code Pulse](https://owasp.org/www-project-code-pulse/)

## Books
- The art of unit testing - Roy Osherov
- TDD by Example - Kent Beck
- XUnit Test Patterns by Gerard Meszaros

# 🧠 Stay curious!
