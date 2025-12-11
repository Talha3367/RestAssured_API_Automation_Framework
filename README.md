# Rest Assured API Testing Framework

This is a **Rest Assured** based API testing framework designed to automate the testing of **RESTful web services**. It supports various types of API tests, such as authentication, CRUD operations, file uploads, and data-driven testing.

## Features

* **API Testing**: Test your REST APIs with ease using Rest Assured.
* **Authentication**: Supports various authentication mechanisms like Basic Auth.
* **Data-Driven Testing**: Allows testing using data from **CSV**, **Excel**, and **JSON** files.
* **Dynamic Test Creation**: Create dynamic test cases using flexible data.
* **Test Retries**: Automatically retry failed tests with custom logic.
* **Custom Listeners**: Includes custom listeners for detailed reporting and enhanced test control.
* **Allure Reports**: Integration with Allure for generating detailed and interactive test reports.

## Project Structure

The framework is organized in the following manner:

```
RestAssuredAPITestingFramework/
├── src/
│   ├── java/
│   │   └── com/testautomation/apitesting/
│   │       ├── listener/                  # Custom listeners for tests
│   │       ├── pojos/                     # POJOs for API requests/responses
│   │       ├── tests/                     # Test classes organized by functionality
│   │       └── utils/                     # Helper classes and constants
│   ├── resources/
│   │   └── suites/                        # TestNG suite files
│   └── pom.xml                            # Maven dependency management
├── test-output/                           # Test output directory (generated after test execution)
└── README.md                              # Project overview and instructions
```

### Key Folders

* **`listener/`**: Contains custom listeners for controlling test execution (e.g., retries, reporting).
* **`pojos/`**: Contains POJOs used for request and response bodies.
* **`tests/`**: Contains various test classes, including basic API tests, file upload tests, data-driven tests, etc.
* **`utils/`**: Utility classes with helper methods for API testing.
* **`suites/`**: Contains **TestNG XML files** to organize and run test suites.

## Prerequisites

Before running the tests, ensure that you have the following installed:

* **Java** (8 or higher)
* **Maven** (for dependency management and building the project)
* **IDE** like **IntelliJ IDEA** or **Eclipse**

## Setup

1. **Clone the Repository**:
   Clone the repository to your local machine:

   ```bash
   git clone <repository-url>
   ```

2. **Install Dependencies**:
   After cloning, navigate to the project folder and run the following Maven command to install the dependencies:

   ```bash
   mvn clean install
   ```

3. **Import Project into IDE**:

    * If using **Eclipse**: Import the project as a **Maven Project**.
    * If using **IntelliJ IDEA**: Open the project directly or import as a **Maven Project**.

## Running Tests

You can run the tests either from your **IDE** or from the **command line**.

### Running Tests from IDE:

* Right-click on the **TestNG XML file** (e.g., `restassuredapitest.xml`).
* Select **Run As → TestNG Suite** to run the tests.

### Running Tests from Command Line:

To run tests from the command line, navigate to the root folder of the project and execute:

```bash
mvn test
```

## Test Suites

The project contains multiple **TestNG XML files** to run different sets of tests:

* **`restassuredapitest.xml`**: Main suite for standard API operations.
* **`datadriventestingusingcsv.xml`**: Data-driven testing using CSV data.
* **`datadriventestingusingexcel.xml`**: Data-driven testing using Excel data.
* **`retrytest.xml`**: Suite that demonstrates test retries in case of failure.

## Report Generation

Once the tests are executed, the framework generates **Allure Reports** that provide detailed insights on test execution, including successes, failures, and execution time.

To generate the report, run the following command:

```bash
allure serve
```

This will start a local server and open the Allure report in your browser.

## Conclusion

This framework is designed to streamline the process of testing REST APIs with a clean structure, supporting dynamic tests, retries, and detailed reporting. It's ideal for any API testing needs, whether you're automating simple API calls or working with large data sets.

