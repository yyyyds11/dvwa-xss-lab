# 🎯 Reflected XSS 漏洞复现报告

## ✅ 漏洞类型

Reflected XSS（反射型跨站脚本）

## 🧪 测试靶场

- DVWA v1.10（低安全级别）
- Kali Linux 物理机
- 本地访问地址：http://localhost/DVWA

## 🛠️ 渗透步骤

1. 登录 DVWA 后，点击左侧菜单「XSS (Reflected)」
2. 在输入框中输入以下内容并提交：

```html
<script>alert('XSS 成功')</script>
```
