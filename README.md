# 电气创新协会网站 修改操作手册
> 面向网页修改初学者，目标：仅更新网页展示内容，**不改动页面样式、布局、JS逻辑**
> ⚠️ 修改前必做：备份原文件！复制整套文件存一份备份，改错可以直接还原。

## 文件总览
| 文件名 | 作用 | 修改方式 |
|------|------|--------|
| `index.html` | 网站首页 | 直接改HTML内部文字，不动`<style>`与`<script>` |
| `GuanYuXieHui.html` | 关于协会页面 | 直接改HTML内部文字，不动`<style>`与`<script>` |
| `notice.html` | 公告动态页面 | **禁止修改此文件**，公告数据统一维护 `notices.json` |
| `notices.json` | 公告数据源 | 增删改公告只操作这个JSON文件 |
| `1.html` | 发展成果页面 | **禁止修改此文件**，项目数据统一维护 `projects.json` |
| `projects.json` | 项目成果数据源 | 增删改项目只操作这个JSON文件 |
| `images/` | 图片存放文件夹 | 所有图片资源放这里 |

## 工具推荐
1. 编辑器：VS Code（免费），不要使用系统记事本，容易出现中文乱码。
2. 本地预览：安装 Live Server 插件，右键HTML文件 → `Open with Live Server`，浏览器实时查看效果。
3. 文件保存编码：全部设置为 `UTF‑8`，否则中文会乱码。

> ✅ 核心规则
> - 更新公告、新增项目成果：只改 `.json` 数据文件
> - 更新首页/关于协会大段固定文字：修改对应 `.html`
> - ❌ 不要修改 `<style>`、`<script>` 内部代码，会造成页面布局错乱、功能失效。

---

## 1. 更新公告动态（notices.json）
> notice.html页面自动读取本JSON渲染公告，**不要修改notice.html**

### 字段释义
```json
{
  "id": "p4",
  "isTop": true,
  "title": "2024年秋季纳新宣讲会即将开启",
  "desc": "零基础可参与，不限专业！宣讲会将详细介绍协会的三大核心技术赛道...",
  "date": "2024-09-15",
  "location": "智能制造与材料学院报告厅",
  "tag": "置顶公告",
  "tagColor": "green",
  "link": "https://www.baidu.com",
  "isExpired": false
}