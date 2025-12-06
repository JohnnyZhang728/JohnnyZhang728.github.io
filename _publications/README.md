# Publications 管理指南

## 📝 新增 Publication 条目

### 步骤 1: 创建新的 Markdown 文件

在 `_publications/` 目录下创建一个新的 `.md` 文件，文件名建议使用论文标题的缩写（大写字母），例如：
- `SPPNET.md`
- `MY_NEW_PAPER.md`

### 步骤 2: 准备论文图片（可选）

1. 将论文的 teaser 图片放到 `images/` 目录下
2. 图片文件名建议使用小写字母和下划线，例如：`sppnet_teaser.png`

### 步骤 3: 填写文件内容

复制以下模板并填写相应信息：

```markdown
---
title: "你的论文标题"
collection: publications
category: conferences  # 或 manuscripts, books
link: https://your-paper-url.com  # 论文的网页链接（可选）
permalink: /publications/YOUR_PAPER_NAME
excerpt: '这里是论文的摘要，会显示在publications列表页面。'
date: 2024-01-01  # 发表日期，格式：YYYY-MM-DD
venue: '会议或期刊名称'
paperurl: 'http://JohnnyZhang728.github.io/files/your-paper.pdf'  # PDF链接（可选）
authors: '作者1, 作者2, 作者3'  # 作者列表（可选，如果没有会从citation中提取）
citation: '完整的引用格式，例如：Author1, Author2, and Author3 (2024). "Paper Title." In Conference Name (pp. 1-10).'
header:
  teaser: your_image_name.png  # 图片文件名（放在images目录下，可选）
---

这里是论文的详细描述。当用户点击论文标题进入详情页时，这里的内容会显示。
```

### 步骤 4: 字段说明

| 字段 | 必填 | 说明 | 示例 |
|------|------|------|------|
| `title` | ✅ | 论文标题 | `"SPPNet: A Single-Point Prompt Network"` |
| `collection` | ✅ | 必须为 `publications` | `publications` |
| `category` | ✅ | 分类：`conferences`, `manuscripts`, `books` | `conferences` |
| `permalink` | ✅ | 唯一URL路径 | `/publications/SPPNET` |
| `excerpt` | ✅ | 摘要（显示在列表页） | `'论文摘要...'` |
| `date` | ✅ | 发表日期（必须使用完整格式YYYY-MM-DD，显示时只会显示年份） | `2024-01-01` |
| `venue` | ✅ | 会议/期刊名称 | `'MICCAI-MLMI'` |
| `link` | ❌ | 论文网页链接 | `https://doi.org/...` |
| `paperurl` | ❌ | PDF文件链接 | `'http://.../paper.pdf'` |
| `authors` | ❌ | 作者列表 | `'Author1, Author2'` |
| `citation` | ❌ | 完整引用格式 | `'Author (2024). "Title."...'` |
| `header.teaser` | ❌ | 图片文件名 | `sppnet_teaser.png` |

### 步骤 5: 上传PDF文件（如果有）

如果提供 `paperurl`，需要：
1. 将PDF文件放到 `files/` 目录下
2. 在 `paperurl` 字段中使用完整URL：`http://JohnnyZhang728.github.io/files/your-paper.pdf`

### 步骤 6: 提交并推送

```bash
cd JohnnyZhang728.github.io
git add _publications/YOUR_PAPER_NAME.md
git add images/your_image.png  # 如果有图片
git add files/your-paper.pdf    # 如果有PDF
git commit -m "Add new publication: YOUR_PAPER_NAME"
git push origin master
```

---

## ✏️ 修改现有 Publication 条目

### 步骤 1: 找到要修改的文件

在 `_publications/` 目录下找到对应的 `.md` 文件

### 步骤 2: 编辑文件

直接修改文件中的字段值即可。例如：
- 修改标题：更改 `title` 字段
- 更新链接：修改 `link` 或 `paperurl`
- 更换图片：修改 `header.teaser` 并替换 `images/` 目录下的图片文件

### 步骤 3: 提交更改

```bash
cd JohnnyZhang728.github.io
git add _publications/FILENAME.md
git commit -m "Update publication: FILENAME"
git push origin master
```

---

## 🖼️ 关于图片

### 添加图片的步骤：

1. **准备图片**
   - 建议尺寸：宽度 200-400px
   - 格式：PNG, JPG 都可以
   - 文件名：使用小写字母和下划线

2. **放置图片**
   - 将图片放到 `images/` 目录下

3. **在文件中引用**
   ```yaml
   header:
     teaser: your_image_name.png
   ```
   - 只需要文件名，不需要路径
   - 系统会自动从 `/images/` 目录加载

4. **提交图片**
   ```bash
   git add images/your_image_name.png
   git commit -m "Add teaser image for publication"
   git push origin master
   ```

---

## 📋 完整示例

```markdown
---
title: "My Awesome Paper: A Novel Approach"
collection: publications
category: conferences
link: https://doi.org/10.1234/example
permalink: /publications/MY_AWESOME_PAPER
excerpt: 'This paper presents a novel approach to solving an important problem. We propose...'
date: 2024-03-15
venue: 'ICML 2024'
paperurl: 'http://JohnnyZhang728.github.io/files/my_awesome_paper.pdf'
authors: 'Zeyu Zhang, Co-Author1, Co-Author2'
citation: 'Zhang, Z., Author1, A., and Author2, B. (2024). "My Awesome Paper: A Novel Approach." In International Conference on Machine Learning (pp. 123-456).'
header:
  teaser: my_awesome_paper_teaser.png
---

## Abstract

This is the detailed description of the paper. Users will see this content when they click on the paper title to view the full page.

## Contributions

- Contribution 1
- Contribution 2
- Contribution 3

## Results

Our method achieves state-of-the-art performance...
```

---

## ⚠️ 注意事项

1. **文件名**：使用大写字母和下划线，例如 `MY_PAPER.md`
2. **permalink**：必须唯一，建议与文件名对应（去掉 `.md`）
3. **日期格式**：必须使用 `YYYY-MM-DD` 格式（如 `2023-10-10`），不能只写年份。虽然显示时只会显示年份，但Jekyll需要完整的日期格式才能正确解析。
4. **图片路径**：只需要文件名，系统会自动从 `images/` 目录加载
5. **PDF路径**：如果放在 `files/` 目录，使用完整URL：`http://JohnnyZhang728.github.io/files/filename.pdf`
6. **按钮行为**：
   - 如果有 `paperurl`，[Paper] 按钮会跳转到PDF
   - 如果没有 `paperurl`，[Paper] 按钮会跳转到publications列表页
   - 如果有 `link`，[Webpage] 按钮会跳转到外部链接
   - 如果没有 `link`，[Webpage] 按钮会跳转到publications列表页

---

## 🔍 查看效果

1. **本地预览**（如果安装了Jekyll）：
   ```bash
   bundle exec jekyll serve
   ```
   然后访问 `http://localhost:4000/publications/`

2. **在线查看**：
   - 推送后等待几分钟
   - 访问：`https://JohnnyZhang728.github.io/publications/`

