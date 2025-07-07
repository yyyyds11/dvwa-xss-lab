# 💥 DVWA Reflected XSS Vulnerability Reproduction

[![Language](https://img.shields.io/badge/language-PHP-blue)](https://www.php.net/)
[![Platform](https://img.shields.io/badge/platform-Kali%20Linux-red)](https://www.kali.org/)
[![License](https://img.shields.io/badge/license-Open-brightgreen)]()
[![DVWA](https://img.shields.io/badge/DVWA-v1.10-orange)](https://github.com/digininja/DVWA)

> 🎯 This project demonstrates a **Reflected XSS (Cross-site Scripting)** vulnerability reproduction in the DVWA lab environment. It is designed as a beginner-friendly Web security practice project.

---

## ✅ Objectives

- Understand the principles of Reflected XSS vulnerabilities  
- Learn how to manually craft XSS payloads in DVWA  
- Document the testing process in a structured security report  
- Use this as a portfolio item for cybersecurity job applications

---

## 💻 Environment

| Component | Description             |
| --------- | ----------------------- |
| OS        | Kali Linux (bare metal) |
| Web App   | DVWA v1.10              |
| Server    | Apache2 + PHP           |
| Database  | MariaDB                 |
| Browser   | Firefox                 |
| Language  | PHP / HTML              |

---

## 🧪 Reproduction Steps

1. Log in to DVWA and navigate to `XSS (Reflected)` module.
2. In the input field, submit the following payload:

```html
<script>alert('XSS')</script>
```
3. A JavaScript alert box pops up, indicating that the payload was executed.
    This confirms the presence of a **Reflected XSS** vulnerability.

---

## 📷 Screenshot

```
screenshots/xss_popup.png
```

<div align="center">   <img src="screenshots/xss_popup.png" width="400"/> </div>

---

## 📄 Vulnerability Report

See detailed write-up in [XSS漏洞复现报告.md](report/XSS漏洞复现报告.md)

---

## 🔐 Mitigation Recommendations

- Use `htmlspecialchars()` to encode user outputs
- Implement strict Content Security Policy (CSP) headers
- Sanitize inputs with whitelisting and validation techniques

---

## 🧭 Future Work

- Reflected XSS (this project)
- Stored XSS
- SQL Injection
- CSRF
- File Upload Exploits
- TryHackMe Practical Labs

---

## 🧠 Author Notes

This project was completed as part of a beginner's penetration testing practice using DVWA.
 It is intended to demonstrate basic web vulnerability exploitation and is open for extension and enhancement.

---

## 📫 Contact

Feel free to reach out if you're recruiting for entry-level security roles in Japan or remote:

- GitHub: https://github.com/yyyyds11

---

## 🌏 中文版

你也可以查看中文报告：[README.md](./README.md)
