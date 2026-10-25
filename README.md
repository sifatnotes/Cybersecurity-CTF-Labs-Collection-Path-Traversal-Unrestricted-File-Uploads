# Cybersecurity-CTF-Labs-Collection-Path-Traversal-Unrestricted-File-Uploads
A curated index of hands-on CTF labs covering path traversal filter bypasses (double encoding, Unicode, null byte), Zip Slip, web shell uploads, SVG Stored XSS, and malicious PDF defense from Learn SecByte.
# Path Traversal & Unrestricted File Upload CTF Labs Collection

A structured, searchable index of hands-on cybersecurity labs focusing on path traversal filter bypasses (double encoding, Unicode normalization, null byte truncation, absolute paths), Zip Slip archive extraction attacks, web shell file uploads, and malicious file payload defense hosted on Learn SecByte.

This repository is designed for application security engineers, penetration testers, CTF players, security analysts, and developers learning how to audit, exploit, and remediate file handling and path sanitization vulnerabilities.

---

## Table of Contents
- [Introduction](#introduction)
- [Lab Collection & Index](#lab-collection--index)
- [Categories](#categories)
  - [Path & Directory Traversal Filter Bypasses](#path--directory-traversal-filter-bypasses)
  - [Archive Exploitation & Zip Slip Vulnerabilities](#archive-exploitation--zip-slip-vulnerabilities)
  - [File Upload Misconfigurations & Web Shell Execution](#file-upload-misconfigurations--web-shell-execution)
- [Learning Path](#learning-path)
- [How to Use the Labs](#how-to-use-the-labs)
- [Disclaimer](#disclaimer)

---

## Introduction

Insecure handling of file paths and user-uploaded media represents one of the most common vectors for initial access and remote code execution. Defenses relying on simple string stripping, extension blacklists, or naive path validation are frequently bypassed using encoding tricks, null bytes, or compressed archives.

This repository organizes hands-on cybersecurity labs from Learn SecByte into structured learning paths covering file input validation, path sanitization, and secure media handling.

---

## Lab Collection & Index

| Lab Title | Target Vector | Primary Category | Access Link |
| :--- | :--- | :--- | :--- |
| **Absolute Path Abuse** | File Access | Path Traversal | [Access Lab](https://learn.secbyte.org/ctf/absolute-path-abuse) |
| **Double Encoding Traversal** | Encoding Bypass | Path Traversal | [Access Lab](https://learn.secbyte.org/ctf/double-encoding-traversal) |
| **Unicode Traversal** | Encoding Bypass | Path Traversal | [Access Lab](https://learn.secbyte.org/ctf/unicode-traversal-bypassing-path-filters-with-encoding-trick) |
| **Null Byte Traversal** | Truncation Bypass | Path Traversal | [Access Lab](https://learn.secbyte.org/ctf/null-byte-traversal-from-filter-bypass-to-file-exposure) |
| **Path Traversal Basics** | File Access | Path Traversal | [Access Lab](https://learn.secbyte.org/ctf/path-traversal-basics) |
| **Directory Traversal Defense** | Remediation | Path Traversal | [Access Lab](https://learn.secbyte.org/ctf/directory-traversal-defense-and-exploitation) |
| **Malicious PDF Upload Defense** | File Security | File Uploads | [Access Lab](https://learn.secbyte.org/ctf/malicious-pdf-upload-defense-lab) |
| **Zip Slip Path Traversal** | Archive Extraction | Archive Security | [Access Lab](https://learn.secbyte.org/ctf/zip-slip-path-traversal-archive-extraction) |
| **Archive Upload Exploitation** | Archive Extraction | Archive Security | [Access Lab](https://learn.secbyte.org/ctf/archive-upload-exploitation) |
| **Web Shell Upload** | Remote Code Execution | File Uploads | [Access Lab](https://learn.secbyte.org/ctf/web-shell-upload-from-filter-bypass-to-incident-response) |
| **SVG Upload Abuse** | Stored XSS | File Uploads | [Access Lab](https://learn.secbyte.org/ctf/svg-upload-abuse-from-image-uploads-to-stored-xss) |
| **Image Upload Bypass** | Validation Bypass | File Uploads | [Access Lab](https://learn.secbyte.org/ctf/image-upload-bypass-from-validation-failures-to-web-shell-de) |

---

## Categories

### Path & Directory Traversal Filter Bypasses
Hands-on CTF labs detailing path resolution mechanisms, filter evasion techniques, and secure file path validation:

* **Path Traversal Basics:** Core concepts of navigating file systems using directory traversal sequences (`../`).
  * Lab Link: https://learn.secbyte.org/ctf/path-traversal-basics
* **Absolute Path Abuse:** Circumventing relative sanitization checks by providing full filesystem paths (`/etc/passwd`, `C:\Windows\win.ini`).
  * Lab Link: https://learn.secbyte.org/ctf/absolute-path-abuse
* **Double Encoding Traversal:** Bypassing web application firewalls (WAF) and input filters via double URL-encoded traversal sequences (`%252e%252e%252f`).
  * Lab Link: https://learn.secbyte.org/ctf/double-encoding-traversal
* **Unicode Traversal:** Exploiting Unicode normalization behavior in web servers to bypass path restrictions.
  * Lab Link: https://learn.secbyte.org/ctf/unicode-traversal-bypassing-path-filters-with-encoding-trick
* **Null Byte Traversal:** Utilizing null byte injection (`%00`) in legacy language interpreters to truncate file extensions and expose sensitive files.
  * Lab Link: https://learn.secbyte.org/ctf/null-byte-traversal-from-filter-bypass-to-file-exposure
* **Directory Traversal Defense & Exploitation:** Comparing offensive bypass methods against defensive path canonicalization algorithms.
  * Lab Link: https://learn.secbyte.org/ctf/directory-traversal-defense-and-exploitation

### Archive Exploitation & Zip Slip Vulnerabilities
Practical security labs analyzing compressed file processing, path overwrites, and arbitrary file write flaws during archive extraction:

* **Zip Slip Path Traversal:** Crafting malicious ZIP archives containing relative path filenames to overwrite system binaries or web roots upon extraction.
  * Lab Link: https://learn.secbyte.org/ctf/zip-slip-path-traversal-archive-extraction
* **Archive Upload Exploitation:** Exploring various compressed archive formats (TAR, ZIP, GZ) to execute arbitrary file write attacks.
  * Lab Link: https://learn.secbyte.org/ctf/archive-upload-exploitation

### File Upload Misconfigurations & Web Shell Execution
Labs focused on subverting file validation controls, Content-Type checks, MIME-type checks, and media parsing routines:

* **Image Upload Bypass:** Bypassing client-side and server-side image validation checks to drop web shells into public directories.
  * Lab Link: https://learn.secbyte.org/ctf/image-upload-bypass-from-validation-failures-to-web-shell-de
* **Web Shell Upload:** Escalating file upload misconfigurations to remote code execution and conducting incident response analysis.
  * Lab Link: https://learn.secbyte.org/ctf/web-shell-upload-from-filter-bypass-to-incident-response
* **SVG Upload Abuse:** Embedding JavaScript inside vector image formats (SVG) to trigger Stored Cross-Site Scripting (XSS).
  * Lab Link: https://learn.secbyte.org/ctf/svg-upload-abuse-from-image-uploads-to-stored-xss
* **Malicious PDF Upload Defense:** Analyzing embedded JavaScript, active content, and action triggers within user-uploaded PDF files.
  * Lab Link: https://learn.secbyte.org/ctf/malicious-pdf-upload-defense-lab

---

## Learning Path

Follow this structured roadmap to master file security and path validation testing:

1. **Path Traversal Fundamentals & Filter Evasion**
   - Start with basic directory traversal and absolute path references.
   - Practice advanced evasion using double URL encoding, Unicode normalization, and null byte truncation.
2. **Archive Handling & Zip Slip Testing**
   - Study canonical path verification during file uncompression.
   - Craft custom ZIP archives to evaluate path resolution during extraction.
3. **File Upload Filter Bypasses**
   - Test extensions, MIME-types, magic bytes, and polyglot files against upload handlers.
   - Execute web shell payloads and analyze execution boundaries.
4. **Active Content & File Format Hardening**
   - Inspect SVG images for Stored XSS vectors and audit PDF documents for embedded executable objects.
   - Implement strict storage isolation, random file renaming, and non-executable directory permissions.

---

## How to Use the Labs

1. Select a practice scenario from the index table or category sections above.
2. Access the target lab environment directly on Learn SecByte.
3. Utilize web proxies (e.g., Burp Suite) or terminal utilities to manipulate file uploads, encode request parameters, and construct custom archives.
4. Review defensive controls to learn how indirect file references, strict allowlists, and path canonicalization protect software.

---

## Disclaimer

This repository is strictly intended for educational research, authorized security testing, and defensive engineering training. All concepts, techniques, and lab environments are provided to help cybersecurity practitioners identify vulnerabilities and defend systems. Unsanctioned testing or attacks against external infrastructure without prior written authorization are strictly illegal.
