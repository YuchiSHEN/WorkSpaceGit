# 网页内容维护说明

网页使用 GitHub Pages 自带的 Jekyll 构建。具体内容保存在 `_data/cv/*.yml`，页面模板保存在 `index.html`，视觉样式保存在 `styles.css`。

## 为什么使用 YAML

YAML 适合简历中的结构化列表，手工编辑比 JSON 简洁，也比纯文本更容易稳定地表示年份、标题、链接、图片和多段说明。字段中的长文本可以使用 Markdown，例如 `**粗体**`、`*斜体*` 和 `[链接](https://example.com)`。

## 文件对应关系

- `profile.yml`：姓名、职位、联系方式、头像、导航和简介
- `education.yml`：教育经历
- `experience.yml`：工作与博士后经历
- `research.yml`：基金与研究项目
- `publications.yml`：论文
- `awards.yml`：奖项与荣誉
- `activities.yml`：专业活动与工作坊
- `developments.yml`：开发工具、链接与项目图片
- `statement.yml`：个人陈述和签名图片

## 增减条目

列表内容都位于 `items:` 或 `paragraphs:` 下。复制一个完整的 `-` 条目即可新增；删除完整条目即可移除。例如：

```yaml
items:
  - year: "2026"
    title: Example Award
    description: Award description.
```

YAML 使用空格缩进，不能使用 Tab。包含冒号、`#` 或纯数字年份时，建议使用引号。保存为 UTF-8。

## 替换图片

头像路径由 `_data/cv/profile.yml` 中的 `photo` 字段控制：

```yaml
photo: assets/profile.jpg
```

可以直接替换 `assets/profile.jpg`，文件名和格式保持不变时不需要修改其他文件。项目图片同理由 `developments.yml` 中的 `image` 字段控制。

开发项目的动画素材使用 GIF。替换 `assets/bsim.gif`、`assets/adrfr.gif` 或 `assets/vgs.gif` 后，浏览器会直接播放多帧动画，不需要额外 JavaScript。

## 自动更新流程

修改并推送到 `main` 后，GitHub Pages 会自动运行 Jekyll、读取 YAML 并生成最终 HTML。通常几十秒内上线。浏览器端加载的是构建后的静态页面，不依赖额外 JavaScript 或第三方 Markdown 解析器。
