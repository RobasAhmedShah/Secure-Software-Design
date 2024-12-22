Here’s a **differences table** for the testing methods and strategies to help you visualize and compare them effectively:

| **Testing Type**                  | **Definition**                                                                 | **Purpose**                                        | **Methodology**                               | **Example Use Case**                                                                                  | **Strengths**                                                                                                     | **Limitations**                                                                                 |
|-----------------------------------|---------------------------------------------------------------------------------|---------------------------------------------------|------------------------------------------------|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| **SAST (Static Application Security Testing)** | Analyzes source code or binaries for vulnerabilities.                           | Identify vulnerabilities in code before runtime.  | Static analysis during development or build.  | Detecting SQL injection risks in database queries.                                                   | Early detection of code issues, integration into CI/CD.                                                         | High false positives, cannot detect runtime issues.                                            |
| **DAST (Dynamic Application Security Testing)** | Tests the application in its runtime environment.                              | Identify vulnerabilities during execution.        | Runtime analysis of compiled/interpreted code. | Finding XSS vulnerabilities in live web applications.                                                | Identifies runtime issues, effective for real-world scenarios.                                                  | Cannot pinpoint source code issues, requires a running application.                            |
| **Fuzz Testing**                 | Inputs invalid or random data to test application behavior.                     | Identify crashes and stability issues.            | Automated testing with unpredictable inputs.   | Testing malformed input on an online form leading to crashes.                                        | Excellent for uncovering rare bugs and vulnerabilities.                                                         | Limited coverage of functional aspects, requires careful monitoring of results.                 |
| **SCA (Software Composition Analysis)** | Analyzes software components for vulnerabilities and compliance.               | Manage risk in open-source and proprietary code.  | Automated scans in CI/CD pipelines.            | Identifying outdated libraries with known vulnerabilities.                                            | Ensures compliance, tracks vulnerabilities in dependencies.                                                     | Relies on public vulnerability databases, limited in detecting custom issues.                   |
| **Unit Testing**                 | Tests individual components of the software.                                   | Ensure correct behavior of small code units.      | Automated tests written for specific units.    | Testing login functionality with valid and invalid inputs.                                            | Focused and fast feedback, ensures functional correctness.                                                      | Cannot detect integration or system-wide issues.                                               |
| **Regression Testing**           | Re-tests software to ensure changes don’t break existing functionality.         | Validate stability after updates.                 | Automated or manual re-testing of existing cases. | Ensuring checkout functionality remains intact after adding a payment method.                        | Ensures stability after updates, crucial for continuous deployment.                                               | Time-intensive for manual testing, requires comprehensive test cases.                          |
| **Integration Testing**          | Validates interactions between software modules or systems.                     | Ensure seamless integration and functionality.    | Combines modules and runs test scenarios.       | Verifying API integration between a payment gateway and an e-commerce platform.                      | Identifies interface issues, ensures compatibility across modules.                                               | Does not test individual components in isolation.                                              |
| **IAST (Interactive Application Security Testing)** | Combines static and dynamic testing by monitoring during execution.            | Identify issues in actively used parts of the app.| Agent-based monitoring during runtime.         | Detecting misconfigurations in a shopping cart during manual testing.                                | Combines SAST and DAST advantages, provides real-time feedback.                                                 | Effectiveness depends on application usage and external testing.                              |
| **Manual Testing**               | Human-driven analysis of application security and functionality.                | Identify logical flaws and security gaps.         | Browser, proxy tools, developer tools.         | Detecting privilege escalation vulnerabilities through role testing.                                  | Deep insight into business logic, flexible testing methods.                                                      | Time-consuming, relies on tester expertise.                                                    |
| **Fuzzing**                      | Automated input of unexpected data to trigger crashes.                          | Test robustness and error handling.               | Invalid/random data input into application.    | Testing a file upload field with unsupported formats.                                                | Great for stability testing, uncovers rare edge cases.                                                          | Results require manual validation, lacks functional focus.                                    |
| **Infrastructure Testing**       | Validates underlying infrastructure security.                                   | Detect misconfigurations and missing patches.     | Vulnerability scanning tools.                  | Ensuring all servers are patched against known vulnerabilities.                                       | Ensures infrastructure security, complements application-level tests.                                           | Limited scope on application-specific issues.                                                   |
| **API Testing**                  | Tests API endpoints for security and functionality.                             | Ensure secure and reliable API interactions.      | Automated and manual testing with tools.       | Testing rate-limiting on a login API to prevent brute force attacks.                                  | Targets backend directly, bypasses UI issues.                                                                  | Requires API enumeration, resource-intensive.                                                  |

---

This table should help you "wall off" each type of testing with clarity in your mind. Let me know if you want a specific testing method explained further or added examples!