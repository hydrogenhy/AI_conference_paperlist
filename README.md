# Conference Paper List 🚀

一个面向多个会议的论文雷达页 ✨

它把论文标题、作者、摘要收拢到一个清晰的入口，让你不必在官网里反复搜索，也能快速扫方向、找主题、比对相关工作 🔎

## 特点 💡

- 一页式浏览多个会议论文列表 📄
- 支持在页面中切换会议数据源 🧭
- 支持标题、作者、摘要的模糊搜索 🧠
- 支持片段匹配、缩写匹配和轻微拼写误差 🪄

## 如何使用 🛠️

1. 确保当前目录下有 `index.html`、`paper/conferences.json` 和对应的 txt 数据文件
2. 启动本地 HTTP 服务后打开 `index.html`
3. 输入关键词开始检索
   
## 数据文件 📦

- `paper/conferences.json`：会议数据源清单
- `paper/icml_2026_paper.txt`：ICML 2026 论文列表
- `paper/cvpr_2026_paper.txt`：CVPR 2026 论文列表

## Paper txt 格式 📝

每个会议对应一个 txt 文件，放在 `paper` 文件夹中。当前支持两种分隔方式：

方式一：用分隔线分开每篇论文。

```txt
ID: 1
Title: Paper Title
Link: https://example.com/poster/1
Authors: Author A, Author B
Abstract: Paper abstract text.
--------------------------------------------------------------------------------

ID: 2
Title: Another Paper Title
Link: https://example.com/poster/2
Authors: Author C, Author D
Abstract: Another abstract text.
```

方式二：不写分隔线，直接用新的 `ID:` 开始下一篇论文。

```txt
ID: 1.
Title: Paper Title
Link: https://example.com/poster/1
Authors: Author A, Author B
Abstract: Paper abstract text.

ID: 2.
Title: Another Paper Title
Link: https://example.com/poster/2
Authors: Author C, Author D
Abstract: Another abstract text.
```

字段名建议保持为 `ID`、`Title`、`Link`、`Authors`、`Abstract`。其中 `Title` 和 `Link` 是页面展示所需的核心字段。

## 新增会议 🧩

把新的 txt 放进 `paper` 文件夹，然后在 `paper/conferences.json` 里追加一条：

```json
{
  "id": "neurips-2026",
  "name": "NeurIPS 2026",
  "file": "neurips_2026_paper.txt"
}
```

`file` 可以只写文件名，页面会自动从 `paper` 文件夹读取。

## 目前支持的会议 ✅

- ICML 2026
- CVPR 2026

## 待支持的会议 🗓️

- NeurIPS
- ICLR
- ACL
- EMNLP
- ICCV / ECCV
- AAAI / IJCAI
- KDD
- SIGGRAPH

## 欢迎 Contribution 🤝

欢迎补充新的会议 paper list、修正论文信息、补全 abstract，或改进页面交互。

推荐贡献方式：

1. 把新的会议 txt 放到 `paper` 文件夹。
2. 按上面的格式整理 `ID`、`Title`、`Link`、`Authors`、`Abstract`。
3. 在 `paper/conferences.json` 中追加会议配置。
4. 打开页面确认会议能正常切换、搜索和展示。

## 下一步 🧭

- ~~等待后续补全 abstract 抓取与入库 📥~~
- ~~让摘要更稳定地进入检索权重 🎯~~
