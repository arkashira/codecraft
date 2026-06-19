# TECH_SPEC.md

## Technical Specification

### Overview
`codecraft` is a no-code software development platform that leverages AI to automate coding tasks, enabling non-technical founders and indie hackers to build software quickly and efficiently. The platform allows users to define requirements (e.g., "create a CRUD app with React and PostgreSQL") and generates the corresponding code, which can be reviewed, modified, and deployed.

### Architecture Overview
The system follows a microservices architecture with the following components communicating via REST APIs:
- **Frontend**: A web application built with React
