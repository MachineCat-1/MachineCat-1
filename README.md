# 在此填写姓名

在此填写一句话简介（占位）。例如：某某方向在读，或正在准备公务员考试。请换成你自己的话。

个人主页（开启 GitHub Pages 之后）：<https://machinecat-1.github.io/MachineCat-1/>

> 本仓库名和 GitHub 用户名相同，这份 `README.md` 会显示在你的 GitHub 个人资料页。建议文首就留姓名和一句话；下面的使用说明可以保留，方便以后改页面。详细履历写在 `index.html`，不用写在这里。

## 这是什么

一个简洁的静态个人主页，用来自己填经历。学术、工作、考公都可以用，不是作品集主题。

页面上的学校、单位、项目、论文都是占位，不是谁的真实履历。搜「在此填写」或「占位」就能找到要改的地方。

技术上只有 `index.html` 和 `styles.css`，没有构建步骤，改完文字直接提交即可。

## 怎么改内容

1. 用编辑器打开仓库根目录的 `index.html`。
2. 搜索 `在此填写` 和 `占位`，把这些文字换成你的内容。尖括号里的英文标签不用改。
3. 某一类要多写一条：复制对应的一整块 `<article class="entry">` … `</article>`，再改里面的文字。
4. 不需要的一条：把那一整块 `article` 删掉。
5. 整整一节都不用（例如没有论文和专利）：删掉对应的 `<section>`，并删掉页首导航里指向它的那一项。
6. 头像可选。页首注释里写了怎么把圆标换成 `photo.jpg`。不用照片就保持原样，或删掉圆标那一行。
7. 页顶黄底的「模板提示」在填完后删掉（`class="template-banner"` 那一段）。
8. 颜色若要微调，只改 `styles.css` 开头 `:root` 里的几行。只改文字时不用动这个文件。

各区块在 `index.html` 里的位置：

| 区块 | 位置 |
| --- | --- |
| 姓名、一句话简介 | 页首的 `<h1>` 和 `.tagline`，浏览器标题在 `<title>` |
| 关于我 | `id="about"` |
| 教育经历 | `id="education"` |
| 工作 / 研究经历 | `id="experience"` |
| 项目 | `id="projects"` |
| 论文 / 专利 | `id="publications"` |
| 技能 | `id="skills"` |
| 联系方式 | `id="contact"` |

改完后提交并推送到 `main`。若已经开启 GitHub Pages，等一两分钟页面会更新。

本地想先看效果：用浏览器直接打开 `index.html`，或在仓库根目录执行

```bash
python3 -m http.server 8080
```

然后访问 <http://localhost:8080>。

## 怎么开启 GitHub Pages

1. 打开本仓库的 **Settings → Pages**。
2. 在 **Build and deployment** 里，**Source** 选择 **Deploy from a branch**。
3. **Branch** 选择 `main`，文件夹选择 **/ (root)**，保存。
4. 等一两分钟，站点会出现在：

<https://machinecat-1.github.io/MachineCat-1/>

仓库根目录有一个空文件 `.nojekyll`，用来让 Pages 按原样发布这些 HTML，而不会再用 Jekyll 处理一遍。这个文件留着即可。

## 如果以后改成用户主页

现在的地址带仓库名，是因为仓库叫 `MachineCat-1`。若把仓库改名为 `MachineCat-1.github.io`，同一套文件会变成 GitHub 用户主页，地址变为：

<https://machinecat-1.github.io/>

页面用的是相对路径，改名后不用改 `index.html` 或 `styles.css`。Pages 仍选择 `main` 分支、文件夹 **/ (root)**。
