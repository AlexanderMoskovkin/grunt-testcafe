# grunt-testcafe

>Tests runner

## Getting Started
This plugin requires Grunt `~0.4`.

If you haven't used [Grunt](http://gruntjs.com/) before, be sure to check out the [Getting Started](http://gruntjs.com/getting-started) guide, as it explains how to create a [Gruntfile](http://gruntjs.com/sample-gruntfile) as well as install and use Grunt plugins. Once you're familiar with that process, you may install this plugin with this command:

```shell
npm install grunt-testcafe --save-dev
```

One the plugin has been installed, it may be enabled inside your Gruntfile with this line of JavaScript:

```js
grunt.loadNpmTasks('grunt-testcafe');
```

## The "testcafe" task

### Overview
In your project's Gruntfile, add a section named `testcafe` to the data object passed into `grunt.initConfig()`.

```js
grunt.initConfig({
    testcafe: {
        test: {
            options: {
                files: ['tests/*.test.js'],
                browsers: ['chrome']
            }
        }
    }
})
```

### Options

#### files

*Type*: `Array`

*Default*: `[]`

*Details*: [Configures the test runner to run tests from the specified files.](http://devexpress.github.io/testcafe/documentation/using-testcafe/programming-interface/runner.html#src)

#### browsers

*Type*: `Array`

*Default*: `[]`

*Details*: [Specifying Browsers for Test Task](https://devexpress.github.io/testcafe/documentation/using-testcafe/common-concepts/browser-support.html#specifying-browsers-for-test-task)

*Required*

Configures the test runner to run tests in the specified browsers.

#### reporter

*Type*: `String`

*Default*: `spec`

*Details*: [Reporters](https://devexpress.github.io/testcafe/documentation/using-testcafe/common-concepts/reporters.html)

Specifies the reporter.

#### reporterOutputFile

*Type*: `String`

*Details*: [Reporters](http://devexpress.github.io/testcafe/documentation/using-testcafe/programming-interface/runner.html#saving-the-report-to-a-file)

Specifies the output file path for reporter.

#### filter

*Type*: `function(testName, fixtureName, fixturePath)`

*Default*: `null`

*Details*: [runner.filter](https://devexpress.github.io/testcafe/documentation/using-testcafe/programming-interface/runner.html#filter)

Allows you to manually select which tests should be run.

#### screenshotsPath

*Type*: `String`

*Default*: `null`

*Details*: [Screenshots path](http://devexpress.github.io/testcafe/documentation/using-testcafe/command-line-interface.html#-s-path---screenshots-path)

The path to which the screenshots will be saved. Enables the test runner to take screenshots of the tested webpages.

#### takeScreenshotsOnFail

*Type*: `Boolean`

*Default*: `false`

*Details*: [Take screenshots on fail](http://devexpress.github.io/testcafe/documentation/using-testcafe/command-line-interface.html#-s---screenshots-on-fails)

Specifies if screenshots should be taken automatically whenever a test fails. Requires that the [screenshotsPath](#screenshotsPath) is set.

#### skipJsErrors

*Type*: `Boolean`

*Default*: `false`

*Details*: [Skip JS errors](http://devexpress.github.io/testcafe/documentation/using-testcafe/command-line-interface.html#-e---skip-js-errors)

Defines whether to continue running a test after a JavaScript error occurs on a page (`true`), or consider such a test failed (`false`).

#### quarantineMode

*Type*: `Boolean`

*Default*: `false`

Defines whether to enable the [quarantine mode](https://devexpress.github.io/testcafe/documentation/using-testcafe/programming-interface/runner.html#quarantine-mode).

#### selectorTimeout

*Type*: `Number`

*Default*: `10000`

*Details*: [Selector timeout](http://devexpress.github.io/testcafe/documentation/test-api/selecting-page-elements/selectors.html#selector-timeout)

Specifies the amount of time, in milliseconds, within which [selectors](https://devexpress.github.io/testcafe/documentation/test-api/selecting-page-elements/selectors.html) make attempts to obtain a node to be returned.

#### assertionTimeout

*Type*: `Number`

*Default*: `3000`

*Details*: [Assertion options](http://devexpress.github.io/testcafe/documentation/test-api/assertions/#assertion-options)

Specifies the amount of time, in milliseconds, within which TestCafe makes attempts to successfully execute an assertion if a selector property or a client function was passed as an actual value.
 
#### speed

*Type*: `Number`

*Default*: `1`

*Details* : [Speed factor](http://devexpress.github.io/testcafe/documentation/using-testcafe/command-line-interface.html#--speed-factor)

Specifies the speed of test execution. Should be a number between `1` (the fastest) and `0.01` (the slowest).

#### startApp

*Type*: `Object { command, initDelay  }`

*Default*: `{ initDelay: 1000 }`

*Details* : [startApp](http://devexpress.github.io/testcafe/documentation/using-testcafe/programming-interface/runner.html#startapp)

Specifies a shell command that will be executed before running tests. Use it to launch or deploy the application that will be tested. 

## Contributing
In lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests for any new or changed functionality. Lint and test your code using [Grunt](http://gruntjs.com/).

## License

[The MIT License](LICENSE.txt)
