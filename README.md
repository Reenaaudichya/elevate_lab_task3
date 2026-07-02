# elevate_lab_task3
# Cybersecurity Task 3: Vulnerability Assessment

## Objective
To perform a basic vulnerability assessment on the local machine environment to identify potential security risks and outdated packages using industry-standard tools.

## Tools Used
* **Safety CLI**: An open-source tool used to scan Python dependencies for known security vulnerabilities.

## Methodology
1. **Initial Environment Setup**: Installed the `safety` tool using `pip`.
2. **Vulnerability Scanning**:
   - [cite_start]Executed the `safety check` command to scan installed Python packages for vulnerabilities[cite: 3, 6, 9].
   - Performed an authenticated `safety scan` to cross-reference dependencies against the Safety platform vulnerability database.
3. [cite_start]**Report Analysis**: Reviewed the identified vulnerabilities, focusing on those affecting critical system components like `pip` and various development libraries[cite: 13].

## Key Findings
* [cite_start]**Total Vulnerabilities**: 41 reported vulnerabilities across 14 packages[cite: 13].
* **Critical Issues**: 
    * [cite_start]`pip` (version 25.2) identified with multiple vulnerabilities including Path Traversal and Interpretation Conflicts (CVE-2026-1703, CVE-2026-3219, CVE-2026-6357)[cite: 13].
    * [cite_start]`GitPython` (version 3.1.46) flagged for multiple Remote Code Execution (RCE) and Argument Injection vulnerabilities[cite: 13].
    * [cite_start]`aiohttp` (version 3.13.3) showed vulnerabilities related to HTTP Request Smuggling and Denial of Service (DoS)[cite: 13].

## Remediation Steps
1. [cite_start]**Update Core Tools**: Immediately upgrade `pip` to the latest stable version to mitigate path traversal risks[cite: 13].
2. **Dependency Management**: Review the `requirements.txt` file and update identified vulnerable packages (Pillow, LangChain, GitPython) to their patched versions.
3. [cite_start]**Policy Implementation**: Utilize the Safety Platform dashboard to track ongoing vulnerabilities and automate future scans[cite: 13].

## Reflections/Interview Answers
* [cite_start]**What is vulnerability scanning?** It is an automated process that identifies known security weaknesses in software, configurations, or networks[cite: 20].
* [cite_start]**What is a false positive?** An error where a scanner incorrectly flags a secure component as vulnerable, requiring manual verification[cite: 26].
* [cite_start]**How do you prioritize vulnerabilities?** I prioritize based on the CVSS score and the potential impact on the system’s integrity and availability[cite: 27, 28].
