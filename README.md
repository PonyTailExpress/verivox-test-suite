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


## Setup and Installation

1. **Clone the Repository**:
   
   git clone https://github.com/<your-username>/verivox-test-suite.git
   cd verivox-test-suite

2. **Install Dependencies**:
   
   npm install
   
## Running the Test Suite
   
1. **Run the tests**:

   npm test

2. **Generate the HTML Report**:

   npm run generate-report

## Configuration Files

- 'playwright.config.js': Configuration for Playwright.
- 'cucumber.js': Configuration for Cucumber.
- 'generate-report.js': Script to generate an HTML report from the JSON report.

  
### Conclusion

Following these steps will help you set up and run the project locally and provide comprehensive instructions for others to use and understand the project. This setup ensures that the project is easily shareable and maintainable.


   
   
