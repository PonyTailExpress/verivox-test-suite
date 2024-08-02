# Verivox Test Suite

This project automates testing for the Privathaftpflicht calculator on the Verivox website using Cucumber for Behavior-Driven Development (BDD) and Playwright for browser automation. The test suite produces both human-readable and machine-readable test results.

## Project Structure

verivox-test-suite/
├── features/
│ ├── privathaftpflicht_calculator.feature
├── steps/
│ ├── Privathaftpflicht_calculator_steps.js
├── reports/
│ ├── cucumber_report.json
│ ├── cucumber_report.html
├── playwright.config.js
├── cucumber.js
├── generate-report.js
├── package.json
└── README.md

## Prerequisites

Ensure you have the following installed on your machine:

1. **Node.js** (v12.x or later): You can download and install Node.js from [nodejs.org](https://nodejs.org/).
2. **npm**: npm is included with Node.js installation.

## Setup and Installation

1. **Clone the Repository**:
   
   git clone https://github.com/PonyTailExpress/verivox-test-suite.git
   cd verivox-test-suite

2. **Install Dependencies**:
   
   npm install

2. **Install Playwright**:

   npx playwright install
   
## Running the Test Suite
   
1. **Run the tests**:

   npm test

2. **Generate the HTML Report**:

   npm run generate-report

## Configuration Files

**playwright.config.js**

  This configuration file sets up Playwright's browser settings. Here, you can configure headless mode, viewport size, and other settings.

module.exports = {
  use: {
    headless: false, // Set to true if you want to run tests in headless mode
    viewport: { width: 1280, height: 720 },
    ignoreHTTPSErrors: true,
  },
};
  
**cucumber.js**
This file configures Cucumber to generate both JSON and pretty format reports.

module.exports = {
  default: `--format json:./reports/cucumber_report.json --format pretty`
};

**generate-report.js**
This script generates an HTML report from the JSON report produced by Cucumber.

const reporter = require('cucumber-html-reporter');

const options = {
  theme: 'bootstrap',
  jsonFile: './reports/cucumber_report.json',
  output: './reports/cucumber_report.html',
  reportSuiteAsScenarios: true,
  launchReport: true,
  metadata: {
    "App Version": "1.0.0",
    "Test Environment": "STAGING",
    "Browser": "Chrome  91.0.4472.124",
    "Platform": "Windows 10",
    "Parallel": "Scenarios",
    "Executed": "Remote"
  }
};

reporter.generate(options);

  
### Conclusion

Following these steps will help you set up and run the project locally and provide comprehensive instructions for others to use and understand the project. This setup ensures that the project is easily shareable and maintainable.


   
   
