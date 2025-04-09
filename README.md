## Postman Newman GitHub Actions Integration

This repository demonstrates the integration of Postman collections with GitHub Actions for automated API testing and report generation. The workflow includes running tests on a mock REST API server and generating an enhanced HTML report using Newman and the htmlextra reporter.

## Key Features

Mock REST API Testing: Local server for testing products, orders, and users endpoints with support for GET, POST, PUT, and DELETE methods.
Postman Integration Tests: Includes automated tests for status codes, pagination, sorting, response time, and JSON schema validation following the AAA approach (Arrange, Act, Assert).
GitHub Actions Workflow: Automated execution of Postman tests and generation of a detailed HTML report.
GitHub Pages Deployment: The generated HTML report is published via GitHub Pages for easy access.