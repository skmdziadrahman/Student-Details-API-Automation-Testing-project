# API Automation Testing for Student Details Project

![Postman](https://img.shields.io/badge/Postman-API%20Testing-FF6C37?logo=postman&logoColor=white)
![Newman](https://img.shields.io/badge/Newman-CLI%20Runner-00A98F)
![JavaScript](https://img.shields.io/badge/JavaScript-Test%20Scripts-F7DF1E?logo=javascript&logoColor=black)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-CI-2088FF?logo=githubactions&logoColor=white)

An end-to-end API automation testing project for the **Student Details API** using **Postman, JavaScript, Newman, dynamic test data, request chaining, automated assertions, HTML reporting, and GitHub Actions CI**.

The collection validates student creation, retrieval, update, technical skills creation, address creation, and final combined student details.

## Project Objective

The objective of this project is to demonstrate practical API automation testing skills by validating a complete student-data workflow through reusable Postman requests and automated JavaScript assertions.

The project demonstrates:

- REST API automation using Postman
- Student record creation and retrieval
- Student record update validation
- Dynamic test-data generation
- Environment variable management
- Request chaining using dynamically generated student IDs
- Technical skills data creation
- Student address creation
- Combined student-details validation
- Status code validation
- Response time validation
- Response size validation
- Content-Type validation
- Response structure validation
- Data type validation
- Date format and valid-date validation
- Newman CLI execution
- HTML test reporting
- Continuous Integration with GitHub Actions

## System Under Test

**API:** The Testing World Student Details API  
**Base URL:** `https://thetestingworldapi.com/api`

## API Workflow

| # | Request | Method | Purpose |
|---|---|---|---|
| 1 | Get Student | GET | Retrieve all student records |
| 2 | Create Student | POST | Create a new student with dynamic data |
| 3 | Get Specific Student | GET | Retrieve and validate the newly created student |
| 4 | Update Student | PUT | Update the created student's details |
| 5 | Create Technical Skills | POST | Add technical skills linked to the student |
| 6 | Create Student Address | POST | Add address and phone information linked to the student |
| 7 | FINAL STUDENT DETAILS | GET | Retrieve and validate the complete combined student record |

## Project Structure

```text
API-Automation-Testing-for-Student-Details-Project/
├── .github/
│   └── workflows/
│       └── newman-tests.yml
├── postman/
│   ├── StudentDetailsAPITest.postman_collection.json
│   └── StudentDetailsAPITest.postman_environment.json
├── reports/
│   └── StudentDetailsAPITest_Newman_Report.html
├── .gitignore
├── package.json
└── README.md
```

## Dynamic Test Data

The collection uses Postman dynamic variables and pre-request scripts to generate reusable student data such as:

- First name
- Middle name
- Last name
- Date of birth
- Technical skill values
- Experience dates
- Address data
- Mobile numbers
- Standard codes

Example Postman dynamic variables include:

```javascript
{{$randomNamePrefix}}
{{$randomFirstName}}
{{$randomLastName}}
{{$randomCity}}
{{$randomCountryCode}}
{{$randomStreetAddress}}
```

The student date of birth is also generated dynamically in `DD-MM-YYYY` format.

## Request Chaining

The ID returned by `Create Student` is stored in:

```text
{{Student_id}}
```

This variable is reused across subsequent requests, including:

- Get Specific Student
- Update Student
- Create Technical Skills
- Create Student Address
- FINAL STUDENT DETAILS

This allows the entire API workflow to execute automatically without manually copying student IDs.

## Environment Variables

Important environment variables include:

| Variable | Purpose |
|---|---|
| `base_url` | API base URL |
| `Student_id` | Dynamically created student ID |
| `first_name` | Student first name |
| `middle_name` | Student middle name |
| `last_name` | Student last name |
| `date_of_birth` | Student date of birth |
| `language1` | First generated technical skill |
| `language2` | Second generated technical skill |
| `yearexp` | Technical experience value |
| `lastused` | Last-used value |
| `House_Number` | Generated house number |
| `City` | Generated city |
| `State` | Generated state |
| `Country` | Generated country code |
| `Mobile1` | First generated mobile number |
| `Mobile2` | Second generated mobile number |
| `Std_Code1` | First phone standard code |
| `Std_Code2` | Second phone standard code |
| `Address1` | First generated address |
| `Address2` | Second generated address |

## Assertions Covered

The project contains automated validations for:

- HTTP status codes
- Response times
- Response sizes
- Content-Type
- Non-empty response bodies
- Student ID existence
- Student ID data type
- Required student properties
- First, middle, and last name validation
- Date of birth validation
- API status property validation
- API message validation
- Response object structure
- TechnicalDetails array validation
- Technical detail properties
- Technical ID data type
- Language array validation
- Language value data types
- Experience date format
- Last-used date format
- Student ID relationships
- Address array validation
- Permanent address structure
- Address field data types
- Phone number array structure
- Phone number properties
- Mobile number validation
- Current address null/object handling
- Final combined student-data validation

## Prerequisites

Install:

- Node.js
- npm
- Git
- Postman

Verify your installation:

```bash
node --version
npm --version
git --version
```

## Installation

Clone the repository:

```bash
git clone https://github.com/YOUR-USERNAME/API-Automation-Testing-for-Student-Details-Project.git
```

Navigate to the project:

```bash
cd API-Automation-Testing-for-Student-Details-Project
```

Install dependencies:

```bash
npm install
```

## Run Tests with Newman

Run the complete collection:

```bash
npm test
```

Equivalent Newman command:

```bash
npx newman run postman/StudentDetailsAPITest.postman_collection.json   -e postman/StudentDetailsAPITest.postman_environment.json
```

## Generate HTML Test Report

Run:

```bash
npm run test:report
```

The generated report will be saved to:

```text
reports/StudentDetailsAPITest_Newman_Report.html
```

## Current Test Result

The included Newman report shows:

- **7 requests**
- **106 assertions**
- **106 passed**
- **0 failed**
- **0 skipped**
- **2.5 seconds total run duration**
- **251 ms average response time**
- **11.48 KB total data received**

This represents a fully passing automated API test execution.

## Continuous Integration

The repository includes a GitHub Actions workflow:

```text
.github/workflows/newman-tests.yml
```

The workflow automatically runs the Newman test suite when:

- Code is pushed to the `main` branch
- A pull request targets the `main` branch

This helps ensure automated API regression tests continue to pass after repository changes.

## Recommended Test Evidence

For a professional QA portfolio repository, include:

- Postman collection overview screenshot
- Passing Newman CLI execution screenshot
- Newman HTML report summary screenshot
- GitHub Actions successful workflow screenshot

## Technologies Used

- Postman
- JavaScript
- Newman
- Newman HTML Extra Reporter
- Node.js
- npm
- Git
- GitHub
- GitHub Actions
- REST API

## Skills Demonstrated

- API Testing
- API Automation Testing
- REST API Validation
- Postman Collections
- Postman Environments
- JavaScript Assertions
- Pre-request Scripts
- Dynamic Test Data
- Request Chaining
- CRUD Testing
- Nested JSON Validation
- Data Type Validation
- Date Validation
- Response Structure Validation
- Newman CLI
- Test Reporting
- Continuous Integration

## Author

**Sk Md Ziad Rahman**

QA Portfolio Project

## Acknowledgement

This project uses The Testing World Student Details API for portfolio testing purposes.
