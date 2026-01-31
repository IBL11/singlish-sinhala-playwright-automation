# IT23347762_ASSIGNMENT_1

## Project Overview

This project is an automated testing solution developed as part of the University Assignment. It focuses on implementing automated functional testing using Playwright with JavaScript and Node.js. The project is designed to demonstrate how modern test automation frameworks can be used to validate application behavior efficiently and reliably.

The testing approach follows a data-driven methodology where test scenarios and expected results are maintained externally in JSON files. These JSON files are generated from an Excel source, allowing test data to be updated easily without modifying the test logic. This separation improves maintainability and reduces the risk of errors during test execution.


---


## Purpose of the Project

The purpose of this project is to:
- Reduce manual testing effort through automation
- Ensure consistent and repeatable test execution
- Validate application features against expected results
- Demonstrate practical knowledge of Playwright and Node.js

This assignment also highlights best practices such as:
- Separation of test logic and test data
- Use of configuration files for flexibility
- Automated reporting for easy result analysis

---

## Key Features

- **Playwright-based automation** for reliable end-to-end testing
- **Data-driven testing** using JSON input files
- **Excel to JSON conversion** for easy test data management
- **HTML test reports** with execution details and logs
- **Modular project structure** for scalability and maintenance

---


## Technologies Used
- **Node.js** (JavaScript runtime)
- **Playwright** (end-to-end testing framework)
- **npm** (package manager)

---

## Prerequisites
Before running this project, ensure you have the following installed on your system:

- **Node.js** (version 16 or higher recommended)
- **npm** (comes bundled with Node.js)

To verify installation:

```bash
node -v
npm -v
```

---

## Project Structure

```
IT23347762_ASSIGNMENT_1/
│
├── .github/                 # GitHub-related configurations
├── node_modules/            # Installed dependencies (auto-generated)
├── playwright-report/       # Playwright HTML test reports
├── scripts/                 # Utility scripts
│   └── excel-to-json.js     # Converts Excel test data to JSON
├── test-data/               # Test input data
│   ├── cases.json
│   └── cases.updated.json
├── test-results/            # Raw test execution results
├── tests/                   # Playwright test specifications
│   ├── capture-expected.spec.js
│   └── swifttranslator.spec.js
├── .gitignore
├── IT23347762_Assignment_1.xlsx  # Source Excel test data
├── package.json             # Project metadata and scripts
├── package-lock.json        # Dependency lock file
├── playwright.config.js     # Playwright configuration
└── README.md                # Project documentation
```

---

## Installation Instructions

Follow the steps below carefully to set up and run the project from scratch.

#### Step 1: Clone the Repository

Open a terminal or command prompt and run:

```bash
git clone <repository-url>
cd IT23347762_ASSIGNMENT_1
```

> Replace `<repository-url>` with the actual GitHub repository URL.

---

#### Step 2: Verify Node.js and npm Installation

Ensure Node.js and npm are installed correctly:

```bash
node -v
npm -v
```

If not installed, download Node.js from the official website and install it before proceeding.

---
#### Step 3: Install Project Dependencies

Install all required dependencies using npm:

```bash
npm install
```

This command will:
- Create the `node_modules` folder
- Install Playwright and all other required packages
- Use `package-lock.json` to ensure version consistency

---

#### Step 4: Install Playwright Browsers

Playwright requires browser binaries to execute tests. Install them using:

```bash
npx playwright install
```

This step is mandatory before running tests for the first time.

---

## Test Execution – Step by Step

Follow the steps below **exactly in order** to run the tests successfully.

#### Step 1: Open the Project in Terminal

Make sure you are inside the project root directory:

```bash
cd IT23347762_ASSIGNMENT_1
```

You should see files such as `package.json`, `playwright.config.js`, and the `tests/` folder.

---

#### Step 2: Ensure Dependencies Are Installed

Confirm that dependencies are installed by checking the `node_modules` folder.

If it does not exist, run:

```bash
npm install
```

Wait until the installation completes without errors.

---

#### Step 3: Ensure Playwright Browsers Are Installed

Run the following command to install required browsers:

```bash
npx playwright install
```

This installs Chromium, Firefox, and WebKit required for test execution.

---

#### Step 4: Run All Automated Tests

Execute all Playwright test cases using:

```bash
npx playwright test
```

Expected behavior:
- All `.spec.js` files inside the `tests/` directory are executed
- Test execution status is shown in the terminal
- Results are saved in the `test-results/` directory

---

#### Step 5: Verify Test Results in Terminal

After execution, verify:
- Passed tests are marked in **green**
- Failed tests are marked in **red** with error details

If failures occur, error logs will indicate the exact test and line number.

---

#### Step 6: Generate and Open HTML Test Report

View the detailed HTML report using:

```bash
npx playwright show-report
```

This will:
- Open the report automatically in your default browser
- Display test status, execution time, screenshots, and logs

The report files are stored in the `playwright-report/` directory.

---

#### Step 7: Run a Single Test File (Optional)

To run a specific test file individually:

```bash
npx playwright test tests/swifttranslator.spec.js
```

or

```bash
npx playwright test tests/capture-expected.spec.js
```

Use this method for debugging or validating individual features.

---

#### Step 8: Re-run Tests After Data Changes (Optional)

If test data is updated:

```bash
node scripts/excel-to-json.js
npx playwright test
```

This ensures tests run using the latest data from the Excel source.

---


#### Step 6: View Test Report

After test execution, generate and view the HTML report:

```bash
npx playwright show-report
```

The report will open in your default browser and is also stored in the `playwright-report/` directory.

---

#### Step 7: Run a Specific Test File (Optional)

To run an individual test file:

```bash
npx playwright test tests/swifttranslator.spec.js
```

or

```bash
npx playwright test tests/capture-expected.spec.js
```

---

#### Step 8: Update Test Data from Excel (Optional)

If test data needs to be updated:

1. Modify `IT23347762_Assignment_1.xlsx`
2. Run the conversion script:

```bash
node scripts/excel-to-json.js
```

3. Updated JSON files will be generated inside the `test-data/` directory

---


## Test Data Management

- Test data is stored in the `test-data/` directory as JSON files.
- The original test data source is maintained in `IT23347762_Assignment_1.xlsx`.
- The script `scripts/excel-to-json.js` can be used to convert Excel data into JSON format if updates are required.

To run the conversion script:

```bash
node scripts/excel-to-json.js
```


## Author

**IT23347762 - Bhagya N L I**

---
