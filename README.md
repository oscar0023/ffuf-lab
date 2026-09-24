# 🔎 FFUF Lab — Web Content Discovery & Fuzzing

> A hands-on cybersecurity lab focused on **FFUF (Fuzz Faster U Fool)** and web content discovery techniques.

![Cybersecurity](https://img.shields.io/badge/Focus-Cybersecurity-orange)
![Tool](https://img.shields.io/badge/Tool-FFUF-black)
![Category](https://img.shields.io/badge/Category-Web%20Security-blue)
![Status](https://img.shields.io/badge/Status-Completed-success)

---

## 📌 About the Project

This repository contains a practical lab designed to explore **FFUF**, a fast web fuzzing tool commonly used for discovering hidden web resources and testing web applications.

The objective of this project is not only to learn FFUF commands, but also to understand how different fuzzing techniques can be combined to improve web content discovery and reduce irrelevant results.

The lab covers the progression from basic enumeration to more advanced FFUF features such as filtering, matchers, recursive fuzzing, POST request fuzzing, virtual host discovery and auto-calibration.

---

## 🎯 Objectives

The main objectives of this lab are to:

* Understand the fundamentals of FFUF.
* Set up a controlled environment for web fuzzing.
* Use wordlists with FFUF.
* Perform directory and resource enumeration.
* Discover potentially hidden web content.
* Understand HTTP status codes returned during enumeration.
* Filter unwanted responses.
* Use matchers to identify interesting responses.
* Perform recursive fuzzing.
* Control recursive fuzzing depth.
* Fuzz POST requests.
* Perform virtual host discovery.
* Understand and use FFUF auto-calibration.

---

## 🧰 Tools & Technologies

| Tool / Technology      | Purpose                                 |
| ---------------------- | --------------------------------------- |
| **FFUF**               | Web fuzzing and content discovery       |
| **SecLists**           | Wordlists for enumeration and fuzzing   |
| **Linux / Kali Linux** | Lab environment                         |
| **Web application**    | Target used for the practical exercises |

---

## 🧪 Lab Topics

### 1. Installation & Lab Setup

The lab begins with the installation and configuration required to use FFUF in a controlled environment.

The setup also includes **SecLists**, which provides useful wordlists for security testing.

---

### 2. Directory Enumeration

Directory enumeration is used to discover resources that may not be directly visible from the application's main interface.

Example areas explored in the lab include:

* `robots.txt`
* Administrative directories
* Hidden web resources

The goal is to understand how wordlists can be used to systematically test possible paths.

---

### 3. HTTP Status Codes

During enumeration, HTTP responses can provide useful information about discovered resources.

The lab examines several common status codes:

| Status Code | Meaning            |
| ----------- | ------------------ |
| `200`       | OK                 |
| `301`       | Moved Permanently  |
| `302`       | Temporary Redirect |
| `403`       | Forbidden          |
| `404`       | Not Found          |

Understanding these responses is important when interpreting FFUF results.

---

### 4. Extension Fuzzing

FFUF can also be used to test different file extensions.

This allows an enumeration process to look beyond directories and identify potentially interesting files or endpoints.

The lab explores extension fuzzing using the `-e` option.

---

### 5. Filtering Techniques

Large fuzzing operations can generate many responses that are not useful.

FFUF provides filtering mechanisms to remove unwanted results automatically.

The lab explores filtering based on characteristics such as:

* HTTP status code
* Response size
* Word count
* Line count

The objective is to reduce noise and focus on potentially relevant results.

---

### 6. Matchers

Matchers work in the opposite direction of filters: instead of removing unwanted results, they allow specific responses to be selected based on defined conditions.

The lab covers matching using:

* HTTP status codes
* Response size
* Word count
* Line count

---

### 7. Advanced Matchers & Modes

The lab also explores more advanced ways of controlling FFUF's result matching and fuzzing behavior.

These techniques help make enumeration more precise and manageable.

---

### 8. Recursive Fuzzing

Recursive fuzzing allows FFUF to continue enumerating directories discovered during the initial scan.

This can help reveal resources located deeper within a web application's directory structure.

The lab also covers how to control the **recursive depth** in order to avoid unnecessary enumeration.

---

### 9. POST Request Fuzzing

Fuzzing is not limited to URLs and GET requests.

The lab includes testing FFUF against **POST requests**, demonstrating how fuzzing can be applied to request parameters and form-based interactions.

---

### 10. Fuzzing Real Requests

The lab also explores fuzzing against realistic HTTP requests.

This helps bridge the gap between basic wordlist-based enumeration and more practical web application testing scenarios.

---

### 11. Virtual Host Discovery

Web servers can host multiple applications or websites on the same IP address.

The lab explores the use of FFUF to identify potentially hidden **virtual hosts**.

This technique can be useful during reconnaissance when multiple hostnames may point to the same server infrastructure.

---

### 12. Auto-Calibration

The final part of the lab explores FFUF's auto-calibration functionality using:

```bash
-ac
```

Auto-calibration can help FFUF identify baseline responses and reduce false positives during fuzzing.

---

## 📂 Repository Structure

```text
ffuf-lab/
│
├── README.md
│
├── FFUF_Lab_Report.pdf
│
├── screenshots/
│   ├── installation/
│   ├── directory-enumeration/
│   ├── filtering/
│   ├── recursive-fuzzing/
│   ├── post-fuzzing/
│   └── virtual-hosts/
│
└── commands/
    └── commands.md
```

> The exact structure can be adapted depending on how the screenshots and commands are organized in the final repository.

---

## 🔬 Methodology

The lab follows a progressive approach:

```text
Installation
     ↓
Lab Setup
     ↓
Directory Enumeration
     ↓
HTTP Status Analysis
     ↓
Extension Fuzzing
     ↓
Filtering
     ↓
Matchers
     ↓
Recursive Fuzzing
     ↓
POST Request Fuzzing
     ↓
Virtual Host Discovery
     ↓
Auto-Calibration
```

This progression makes it possible to start with basic FFUF usage and gradually introduce more advanced techniques.

---

## 📚 What I Learned

Through this lab, I practiced:

* Web content discovery
* Directory enumeration
* Wordlist-based fuzzing
* HTTP response analysis
* Result filtering
* Response matching
* Recursive enumeration
* HTTP POST request fuzzing
* Virtual host discovery
* Reducing false positives during fuzzing

More broadly, the lab helped me understand how automated web enumeration can be structured and refined to obtain more relevant results.

---

## 🛡️ Ethical & Legal Use

This project was performed in a **controlled learning environment** for educational purposes.

FFUF and similar security tools should only be used against:

* Systems you own
* Applications you are explicitly authorized to test
* Dedicated cybersecurity training environments
* CTF/lab platforms where security testing is permitted

Unauthorized scanning or fuzzing of third-party systems may be illegal and can cause unintended impact.

**Always obtain explicit authorization before testing a real-world target.**

---

## 📄 Documentation

A detailed report containing the practical exercises and screenshots is included in this repository:

📘 **[FFUF Lab Report](./FFUF_Lab_Report.pdf)**

The report documents the different stages of the lab and provides visual evidence of the exercises performed.

---

## 🚀 Future Improvements

Possible extensions for this project include:

* Adding more advanced FFUF use cases
* Testing different wordlists
* Comparing wordlist effectiveness
* Automating repetitive fuzzing tasks
* Building a dedicated vulnerable web application for testing
* Integrating FFUF into a broader web reconnaissance workflow
* Documenting additional HTTP methods and parameters
* Creating video demonstrations of selected techniques

---

## 👨🏾‍💻 Author

**Oscar Alidjinou**

Cybersecurity Engineering Student
ENSA Agadir — Morocco

Interested in:

* SOC & Security Operations
* Penetration Testing & Vulnerability Assessment
* Network Security & Infrastructure
* Threat Detection & Analysis
* Linux & System Security

---

## ⭐ Disclaimer

This repository is intended for **education, experimentation and cybersecurity skill development**.

Use these techniques responsibly and only on systems for which you have explicit authorization.
