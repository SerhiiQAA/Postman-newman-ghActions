## Postman Newman GitHub Actions Integration

This repository demonstrates the integration of Postman collections with GitHub Actions for automated API testing and report generation. The workflow includes running tests on a mock REST API server and generating an enhanced HTML report using Newman and the htmlextra reporter.

## Key Features

Mock REST API Testing: Local server for testing products, orders, and users endpoints with support for GET, POST, PUT, and DELETE methods.
Postman Integration Tests: Includes automated tests for status codes, pagination, sorting, response time, and JSON schema validation following the AAA approach (Arrange, Act, Assert).
GitHub Actions Workflow: Automated execution of Postman tests and generation of a detailed HTML report.
GitHub Pages Deployment: The generated HTML report is published via GitHub Pages for easy access.

## Attantion
There are two collections in the repository: petstore.collection.json and store.collection.json
To run the store.collection.json collection, you need to run it using a local server.

## How It Works
1. **Install Newman:**
    ```bash
    npm install -g newman
    ```
This command installs Newman globally, enabling you to run Postman collections from the command line.
1. **Run the local API server:**
    ```bash
    npm run tern-on-api
This command initializes the testing server on http://localhost:3000, serving endpoints for products, orders, and users (for store.collection.json).

1. **Run the Postman collection locally using Newman:**
    ```bash
    newman run petstore.collection.json -r htmlextra --reporter-htmlextra-export docs/index.html

1. **Access the published report via GitHub Pages at:**
    ```bash
    https://<your-username>.github.io/<your-repository>/

## Technologies Used
- Postman & Newman: For API testing and report generation.
- GitHub Actions: For CI/CD automation.
- GitHub Pages: For report hosting.
- Node.js: For dependency management and local server setup.
- htmlextra Reporter: For enhanced, visually appealing test reports.

## Future Improvements
- Add integration with additional public APIs.
- Extend test cases to cover edge scenarios.
- Automate more advanced reporting and monitoring.