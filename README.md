# 💥 DVWA Reflected XSS 漏洞复现练习

[![Language](https://img.shields.io/badge/language-PHP-blue)](https://www.php.net/)
[![Platform](https://img.shields.io/badge/platform-Kali%20Linux-red)](https://www.kali.org/)
[![License](https://img.shields.io/badge/license-Open-brightgreen)]()
[![DVWA](https://img.shields.io/badge/DVWA-v1.10-orange)](https://github.com/digininja/DVWA)

> 🎯 本项目通过 DVWA 靶场环境复现了一个反射型 XSS（Reflected Cross-site Scripting）漏洞，适合作为 Web 安全入门实验项目之一。

---

## ✅ 项目目标

- 理解反射型 XSS 漏洞的成因与原理
- 使用 DVWA 靶场手动构造 XSS 攻击载荷
- 编写报告，作为渗透测试练习作品集的一部分

---

## 🧪 环境信息

| 项目 | 版本 |
|------|------|
| 操作系统 | Kali Linux（物理机） |
| 靶场系统 | DVWA v1.10 |
| Web 服务 | Apache2 + PHP |
| 数据库 | MariaDB |
| 浏览器 | Firefox |
| 语言 | PHP / HTML |

---

## 🛠️ 渗透步骤

1. 登录 DVWA 后，选择左侧菜单：`XSS (Reflected)`
2. 在输入框中输入以下内容并提交：

```html
<script>alert('XSS')</script>
```

3. 点击 Submit 后，弹出浏览器对话框，表示漏洞复现成功。

---

## 📷 漏洞截图

```
screenshots/xss_popup.png
```

<div align="center">   <img src="screenshots/xss_popup.png" width="400"/> </div>

## 📄 漏洞报告

详见：`report/XSS漏洞复现报告.md`

------

## 🔧 修复建议

- 使用 `htmlspecialchars()` 对用户输出进行 HTML 编码
- 配置 CSP（内容安全策略）限制脚本来源
- 对用户输入进行白名单校验

------

## 📚 后续计划

- Reflected XSS（已完成 ✅）
- Stored XSS（持久型 XSS）
- SQL Injection（SQL 注入）
- CSRF（跨站请求伪造）
- File Upload 漏洞
- TryHackMe 靶场实战

------

## 🌐 English Version

[README_EN.md](./README_EN.md)
