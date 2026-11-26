# 个人学术简历主页

网站地址：[https://weiwei-612.github.io/](https://weiwei-612.github.io/)

简历内容、样式和打印功能都在根目录的 `index.html` 中，无需安装依赖或运行构建命令。

## 直接在网页端修改简历

1. 登录自己的 GitHub 账号，打开 [在线编辑 index.html](https://github.com/weiwei-612/weiwei-612.github.io/edit/main/index.html)。也可以从仓库打开 `index.html`，点击铅笔图标。
2. 搜索 `你的姓名`、`Your Name`、`待填写` 和 `TODO`，修改对应文字。保留文字周围的 HTML 标签。姓名需要同时修改页面标题、导航栏、正文和页脚。
3. 点击 **Commit changes**，填写说明，例如 `Update CV`，提交到 `main`。如果选择新建分支，需要将对应 Pull Request 合并到 `main`。
4. 在 [Actions](https://github.com/weiwei-612/weiwei-612.github.io/actions) 查看 Pages 部署结果。部署成功后刷新网站查看修改。

网页端编辑修改的是 HTML 源码。当前页面没有表单式管理后台。GitHub 的源码预览不等同于实际网页效果；可以下载 `index.html` 在浏览器打开预览，或在部署完成后访问网站。

## 首次启用 GitHub Pages

如果网站尚未启用，请打开 [Settings → Pages](https://github.com/weiwei-612/weiwei-612.github.io/settings/pages)，设置：

- **Source**：`Deploy from a branch`
- **Branch**：`main`
- **Folder**：`/ (root)`

点击 **Save**。之后每次向 `main` 提交修改，GitHub Pages 都会自动发布。页面更新可能需要几分钟。

根目录的 `.nojekyll` 表示直接发布静态文件。

## 常见修改

| 内容 | 在 index.html 中查找 |
| --- | --- |
| 姓名 | `你的姓名`、`Your Name` |
| 学校和个人简介 | `class="affiliation"`、`class="intro"` |
| 邮箱和学术链接 | `联系方式 / CONTACT` |
| 研究方向 | `id="research"` |
| 论文 | `id="publications"` |
| 开源项目 | `id="projects"` |
| 教育经历 | `id="education"` |

例如，邮箱可以写成：

```html
<dd><a href="mailto:your.name@example.com">your.name@example.com</a></dd>
```

增加论文时，复制论文区域中完整的 `<article class="entry">...</article>`，再修改标题、作者、年份、简介和链接。文字中的 `&`、`<`、`>` 分别使用 `&amp;`、`&lt;`、`&gt;`。

页面支持手机浏览。点击 **打印 / 保存为 PDF**，在浏览器打印窗口选择保存为 PDF。

模板中的姓名、邮箱、论文和教育时间仍需补齐；学校、研究简介和项目描述来自原模板，请根据实际情况核实修改。

## 官方参考

- [GitHub 在线编辑文件](https://docs.github.com/en/repositories/working-with-files/managing-files/editing-files)
- [配置 GitHub Pages 发布来源](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)
