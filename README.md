# Space Elevator

Fictive project of an application handling a space elevator. This project is used on my [website](https://www.rocknprog.com/en/) and [YouTube channel](https://www.youtube.com/channel/UCJsy2UMYdbwEnYSnWFpsLsA) to explain some concepts of web development.

## Installation

Maven is used as a build automation tool, as well as a dependency manager. To build the application, use : 

```
mvn clean install
```

## Usage

### Execute app

To execute the application, use : 

```
mvn exec:java
```

The app will be running on [http://localhost:8080](http://localhost:8080).

## Contributing

Before contributing to the project, please read our [contribution guide](CONTRIBUTING.md).

### Run tests

Tests are located in `src/test/java/com/rocknprog/spaceelevator`. They are all checked pre-commit and during the CI pipeline. Coverage report are generated using Jacoco during the report built phase.

To run unit tests, use :

```
mvn test
```

### Report code coverage

To report code coverage after testing the app, use : 

```
mvn jacoco:report
```

This will generate `target/site/jacoco/index.html`, which can be opened in any browser.

### Apply code style

Code style is verified at each commit. To apply [Google Java Code Style](https://google.github.io/styleguide/javaguide.html) throughout the source code, use : 

```
mvn git-code-format:format-code -Dgcf.globPattern=**/*
```

To simply check code style, use :

```
mvn git-code-format:validate-code-format -Dgcf.globPattern=**/*
```

### API documentation generation

As said above, all requests for this app are listed on our GitHub Pages. We used RAML 1.0. To render documentation, you must install the `npm`/`yarn` dependencies and start the script : 

```
cd /docs
yarn
```

## License

`CC BY-NC-SA 4.0` : [Attribution-NonCommercial-ShareAlike 4.0 International](LICENSE.md)
