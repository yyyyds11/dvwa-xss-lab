# 🎯 Reflected XSS 漏洞复现报告

## ✅ 漏洞类型

Reflected XSS（反射型跨站脚本）

---

## 🧪 测试靶场

- DVWA v1.10（低安全级别）
- Kali Linux 物理机
- 本地访问地址：http://localhost/DVWA

---

## 🛠️ 渗透步骤

1. 登录 DVWA 后，点击左侧菜单「XSS (Reflected)」
2. 在输入框中输入以下内容并提交：

```html
<script>alert('XSS 成功')</script>
```
3. 页面立即弹出浏览器弹窗（见截图），说明存在反射型 XSS 漏洞。

---

📷 截图

放置路径：./screenshots/xss_popup.png

---

🔧 修复建议

    使用 htmlspecialchars() 对用户输入进行 HTML 编码

    设置 CSP 策略禁止脚本注入

    对输入参数添加白名单校验

---

📌 实验总结

本实验说明了在未进行输入验证和输出转义的页面中，反射型 XSS 可轻易注入。该漏洞可被用于钓鱼、窃取 Cookie 等攻击。
