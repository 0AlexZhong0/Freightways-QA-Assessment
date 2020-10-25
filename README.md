# Freightways Information Services – QA Technical Test

## What are the tests

Using the https://jsonplaceholder.typicode.com/posts endpoint, I have created the following tests:

1. Happy path tests for Create, Read, Update and Delete using valid inputs and validating the response for each.
2. Schema validation of API output for each of the CRUD requests above.
3. A negative test for `GET` https://jsonplaceholder.typicode.com/posts/idontexist.

## Running the tests locally

If you have `newman` installed globally already, running this command in the local directory will execute all the tests:

```bash
newman run tests/typicode_posts.postman_collection.json
```

If not you do not have `newman`, then first install `newman` globally by running `npm i -g newman` and run the command above to execute the tests.

## Running the tests in CI/CD pipeline

The CI/CD platform I am using is Travis CI, first, you will need to have this project in your own Github repository by either forking or creating a new one. Then you can get started with Travis CI by:

1. Go to [Travis-ci.com](https://travis-ci.com/) and [Sign up with GitHub](https://travis-ci.com/signin).
2. Accept the Authorization of Travis CI. You’ll be redirected to GitHub.
3. Click on your profile picture in the top right of your Travis Dashboard, click Settings and then the green Activate button, and select the repository for this project to use with Travis CI.

Now every time you push a new commit to the repository, Travis CI will run the specified tests as defined in `.travis.yml`.

## Importing the tests to Postman

Postman provides a clean UI to inspect the collections and the tests for each request. The following is the steps for how to do so:

1. Open Postman
2. Click `import` in the top-left corner.
3. Upload `typicode_posts.postman_collection.json` in the `tests` folder.
4. Click `import` in the current popup window.

Now you can inspect the collections more easily in Postman.

## Link to my UI automation test suite

[This repo](https://github.com/0AlexZhong0/cypress-react-test-example) contains code example for React UI automation tests using Cypress.

Thank you very much for reading until the end!!!

Alex Zhong, xD.
