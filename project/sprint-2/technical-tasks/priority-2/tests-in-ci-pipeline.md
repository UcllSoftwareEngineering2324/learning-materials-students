# Tests in CI pipeline

All tests are currently ran under a single build step in the CI pipeline.

It can be a good idea to do this stepwise:

* Only run integration tests after unit tests pass
* Only run unit tests in the CI workflow to keep the build fast and run integration tests in a different workflow
* ...

Think of a good strategy to incorporate your tests in your builds.