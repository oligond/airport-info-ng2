# Angular Airport Search

This repository holds the source code for my **Paxlife Coding Challenge**.

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 1.0.0.

It is using [Bootstrap](https://v4-alpha.getbootstrap.com/) for convenient prototype UI design.

## Challenge Description

The Challenge was to design and implement a web application that allowed users to search information about an airport. The app was designed with respect to the following directions.

### Technical Requirements

- Use the Paxlife dedicated API (http://sandbox.paxlife.aero/api/)
- Choose a suitable open-source JS framework and libraries. Please motivate your choice!

### Functional Requirements

These user stories needed to be satisfied:
- As a user, I want to request airport information from a city name or from IATA code.
- As a user, I want to see a detailed view of the requested airport with its name, its IATA and ICAO codes, its country code, and a geolocation on a map component.

### Setting

Expected time budget for the task were 6-8 hours. Trade-offs were allowed, all decisions should be documented. The level of feature completeness, documentation, tests was subject to the participant's own decision making. "Product Management is in vacation and not available".

### Mockup

The expected result should approximately look like this:

![Airport Info Mockup](/mockup.jpg)

## Live Demo

See the [app in action](https://alcofribas.github.io/airport-info-ng2/).

## Comments on this solution

### Why Angular?

There are some reasons that brought me to choosing Angular for the task. Most relevant for my decision were aspects offered by Angular which are ultimately related to the sustainability of the product and the development process:

- Componentization/Modularization, Data-Binding, Performance
- Excellent Tooling and Easy Testability
- Suitable for Agile Development and Continuous Integration Strategies

A more difficult question would be why I prefered Angular over other common options with similar advantages. My personal reason here was that I had little knowledge about Angular so far and found it a wonderful opportunity to have a first intense, in-depth encounter with a framework that seemed quite appealing to me on first sight.

### What works

- User stories fulfilled
- Communication with required REST API works
- Overall responsive design and layout

### Where the tradeoffs are

The implementation focused on feature completeness, a mobile first design and a sustainable basic setup for testing and continuous integration. Important tasks like exhaustive error handling and thorough testing were postponed to the next phase of the development process, as well as UI/UX refinement. 

### ToDo

The tradeoffs mentioned above lead to a considerable number of ToDos some of which are pointed out below:

#### Enhancements

- Display message in dropdown while retrieving results asyncronously
- Display message in dropdown when there is no result
- Reset zoom level of map when choosing another airport
- Enable keyboard controls for autocomplete dropdown (Esc, Enter, Arrow Up/Down)
- Support mobile phone touch keyboard form input

#### Optimizations

- Implement elaborate error handling
- Implement proper testing
- Add media queries for best responsive user experience
- Optimize app size and performance
- Have UX guy beautify and streamline UI

#### Cleaning-Up

- Remove in-memory web api including obsolete dependencies
- Remove unneeded Console Logging
- Don't push API key to GitHub ;)

## Dev Prerequisites

Make sure that you have Node.js and npm installed.

<a href="https://docs.npmjs.com/getting-started/installing-node" target="_blank" title="Installing Node.js and updating npm">
Get it now</a> if it's not already installed on your machine.

**Verify that you are running at least node `v4.x.x` and npm `3.x.x`**
by running `node -v` and `npm -v` in a terminal/console window.
Older versions produce errors.

Run the following commands to get started:

```shell
git clone https://github.com/alcofribas/airport-search-ng2
cd airport-search-ng2
npm install
ng serve
```

Point your browser to http://localhost:4200 to start searching for airport information.

### Unit Tests
TypeScript unit-tests are usually in the `src/app` folder. Their filenames must end in `.spec.ts`.

Look for the example `src/app/app.component.spec.ts`.
Add more `.spec.ts` files as you wish; we configured karma to find them.

Run it with `npm test`

That command first compiles the application, then simultaneously re-compiles and runs the karma test-runner.
Both the compiler and the karma watch for (different) file changes.

Shut it down manually with `Ctrl-C`.

Test-runner output appears in the terminal window.
We can update our app and our tests in real-time, keeping a weather eye on the console for broken tests.
Karma is occasionally confused and it is often necessary to shut down its browser or even shut the command down (`Ctrl-C`) and
restart it. No worries; it's pretty quick.

### End-to-end (E2E) Tests

E2E tests are in the `e2e` directory, side by side with the `src` folder.
Their filenames must end in `.e2e-spec.ts`.

Look for the example `e2e/app.e2e-spec.ts`.
Add more `.e2e-spec.js` files as you wish (although one usually suffices for small projects);
we configured Protractor to find them.

Thereafter, run them with `npm run e2e`.

That command first compiles, then simultaneously starts the `lite-server` at `localhost:8080`
and launches Protractor.  

The pass/fail test results appear at the bottom of the terminal window.
A custom reporter (see `protractor.config.js`) generates a  `./_test-output/protractor-results.txt` file
which is easier to read; this file is excluded from source control.

Shut it down manually with `Ctrl-C`.
