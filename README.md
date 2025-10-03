# Cybersecurity-7-Investigating-Suspicious-Browser-Extension-

## I. Executive Summary
The browser audit identified one extension in a critical corrupted state (which was repaired) and flagged a second extension, Mendeley Web Importer, for excessive permissions, violating the Principle of Least Privilege. The unnecessary, high-risk extension was removed. The security analysis confirmed that Length is the single most dominant factor in password strength, a concept reinforced by the need to strictly limit unnecessary attack surfaces in the browser.

### List of Suspicious Extensions Found and Removed (Deliverable)

| Extension Name | Status/Permissions | Security Flag(s) Identified | Action Taken |
| :--- | :--- | :--- | :--- |
| Security WebAdvisor | Corrupted Status initially | Critical State Fixed. The repair eliminated the immediate threat of a failed or unstable security validation. | Repaired & Retained |
| Mendeley Web Importer | "Read and change all your data on all websites." | High Permission, High Risk. Violation of the Principle of Least Privilege. | Removed |
| Save to Pocket | Permissions not fully audited. | Known service, but retained for necessity pending a formal permissions check. | Retained (Pending D-Audit) |
| Google Docs Offline | Pre-installed, trusted source. | Necessary function, low risk. | Retained |
| Google Scholar Button | Low Permission: Only accesses scholar.google.com/*. | Adheres to the Principle of Least Privilege, very low risk. | Retained |

---

### Summary of Browser Performance

| Status | Observation/Finding | Rationale |
| :--- | :--- | :--- |
| Before Audit | The browser had a critical vulnerability (Corrupted Extension) and unnecessary security surface area (High Permissions). | The corrupted state of SecurityExtension could cause instability; the high permissions of Mendeley posed a silent data theft risk. |
| After Audit | Critical corruption fixed. Security surface area significantly reduced by removing the high-risk Mendeley extension. | Eliminating unnecessary high-privilege extensions is the best way to secure the browser against session hijacking or keylogging. |

---

### Analysis: Browser Security (Q&A)

| Question | Expert Answer Summary |
| :--- | :--- |
| **1. How can browser extensions pose security risks?** | They run with elevated privileges, allowing them to perform keylogging, steal session cookies, inject malicious code, and capture data from webpages. |
| **2. What permissions should raise suspicion?** | Any permission that requests more access than necessary (Principle of Least Privilege). The highest risk is "Read and change all your data on all websites." |
| **3. How to safely install browser extensions?** | Use official stores only, verify developer reputation (many users/reviews), and audit requested permissions before installing. |
| **4. What is extension sandboxing?** | A security isolation mechanism that limits the extension's access to the rest of the system and browser, confining the damage a malicious extension can do. |
| **5. Can extensions steal passwords?** | Yes. If an extension has the "read and change all your data" permission, it can function as a keylogger or read authentication tokens from the page. |
| **6. How to update extensions securely?** | Rely on official store updates and **re-audit permissions** after updates, as extensions can be sold to malicious actors (supply chain attack). |
| **7. Difference between extensions and plugins?** | Extensions add features to the UI (e.g., ad blockers). Plugins handle native web content (e.g., Flash) and are mostly obsolete due to security risks. |
| **8. How to report malicious extensions?** | Use the official "Report Abuse" or "Report Misconduct" link provided on the extension's listing page within the browser's Add-ons Store. |

---
### Questions (Evidence-Based Responses)
1. How can browser extensions pose security risks?
Extensions pose risks because they operate with elevated privileges inside the browser's sandbox. A malicious extension can steal data, inject phishing prompts, or perform keylogging (capturing passwords).

2. What permissions should raise suspicion?
Any permission that violates the Principle of Least Privilege is suspicious. The highest-risk permission is:

"Read and change all your data on all websites." (Flagged and removed for the Mendeley Web Importer).

3. Why is password length important?
Password length is the most critical factor because it increases the time required for a brute-force attack exponentially. A short password offers minimal security, whereas a long, high-entropy password moves the estimated time-to-crack to millions of years.

4. What is a dictionary attack?
A dictionary attack is an attempt to crack a password by testing it against a pre-compiled list of common words, phrases, and simple variations. The defense is avoiding common words and patterns to prevent a quick compromise.

5. What is multi-factor authentication (MFA)?
MFA is an authentication method requiring two or more verification factors (something you know, something you have, or something you are) to gain access. It is the essential security layer needed when a password is compromised.

6. How do password managers help?
Password managers generate long, complex, unique, and random passwords that are guaranteed to be high-entropy. They eliminate the biggest security flaws: password reuse and human-created patterns.

7. What are passphrases?
Passphrases are long sequences of random, often unrelated words (e.g., correct-horse-battery-staple). They are considered a best practice because they are high-entropy (due to length) yet relatively easy for a human to remember.

8. What are common mistakes in password creation?
The most common mistakes are password reuse across multiple sites, using sequential patterns on the keyboard, or failing to mix all character types. These mistakes introduce predictability that an attacker can easily guess.
