# CircleCI velocity-cucumber example

Attempting to demonstrate and determine a solution for [this issue](https://github.com/xolvio/meteor-cucumber/issues/128).

Steps to generate this project:

0. **Generate boilerplate**
  ```
  # installed meteor
  meteor create circleci-cucumber-example && cd circleci-cucumber-example
  meteor add xolvio:cucumber
  ```

  then visited http://localhost:3000 and clicked "Add cucumber sample tests"

0. **Get tests to pass in the browser**
  ```
  cd tests/cucumber && npm install # install cucumber dependencies
  ```

  and edited [sample.feature](./tests/cucumber/features/sample.feature) by hand, replacing all instances of "intentional failure" with "circleci-cucumber-example"

0. **Set up the CircleCI build**

  I created a [circle.yml](./circle.yml) copied from [xolvio/Letterpress](https://github.com/xolvio/Letterpress). Then I logged on to circleci.com and configured this repo to build automatically.
