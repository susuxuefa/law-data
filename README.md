<p align="center">
  <img src=".github/assets/banner.svg" alt="法律数据：现行有效司法解释与指导性案例" width="100%">
</p>

<p align="center">
  <a href="https://susujuris.cn/data.html"><img alt="数据页" src="https://img.shields.io/badge/%E6%95%B0%E6%8D%AE%E9%A1%B5-susujuris.cn%2Fdata.html-32689f?style=flat-square"></a>
  <a href="https://github.com/susuxuefa/law-data/releases"><img alt="版本" src="https://img.shields.io/badge/version-v2026.10-c8923f?style=flat-square"></a>
  <img alt="司法解释" src="https://img.shields.io/badge/%E5%8F%B8%E6%B3%95%E8%A7%A3%E9%87%8A-259-2f6f5e?style=flat-square">
  <img alt="指导性案例" src="https://img.shields.io/badge/%E6%8C%87%E5%AF%BC%E6%80%A7%E6%A1%88%E4%BE%8B-279-2f6f5e?style=flat-square">
  <a href="LICENSE"><img alt="许可" src="https://img.shields.io/badge/license-CC%20BY%204.0-8a8f98?style=flat-square"></a>
</p>

<p align="center"><strong>带效力状态的中国法律数据：哪条还有效、案例还能不能引、出处在哪里。</strong></p>

## 为什么会有这个库

法律文本到处都有，难的是三件事：

1. **这条司法解释还有效吗？** 只收现行有效文本；已废止、已被修改的旧文本剔除，并记录依据；
2. **指导案例还能不能引？** 279 篇里 6 篇已被通知「不再参照与适用」，如实标注，不混进正常案例；
3. **引用时怎么给出处？** 每篇带文号／案例编号、公布与施行日期、官方链接，可直接进脚注。

在线阅读与检索：<https://susujuris.cn/data.html>

## 目录

| 路径 | 内容 | 数量 |
|---|---|---|
| `judicial-interpretations/` | 现行有效司法解释全文（Markdown + YAML 头） | 259 |
| `guiding-cases/` | 最高人民法院指导性案例全文（Markdown + YAML 头） | 279 |
| `data/shifashi.json / .csv` | 司法解释元数据 | 259 |
| `data/guiding-cases.json / .csv` | 指导性案例元数据 | 279 |
| `MANIFEST.json` | 版本、数量、来源 | — |
| `STATUS.md` | 收录口径、已知缺口、待办 | — |

字段：

- 司法解释：`n / slug / title / type / fsNo / pubDate / impl / url`
- 指导性案例：`n / title / plain / cause / year / pub / url / kw / laws`

## 怎么用

- **读**：直接打开 Markdown，文件头的 YAML 有文号、日期、效力与官方链接；
- **查**：CSV 用 Excel／WPS 打开，按类型、年份、施行日期筛选；
- **建**：JSON 导入 SQLite／Notion，或作为检索、RAG 的目录层（正文再回官方链接）；
- **引**：

```
苏酥. 最高人民法院现行有效司法解释库（v2026.10）[DB/OL]. 苏酥学法, 2026-10-21.
https://susujuris.cn/data.html.
```

## 版本与更新

版本号形如 `v2026.10`，每次核对在 [STATUS.md](STATUS.md) 记一条变更，并在 [Releases](https://github.com/susuxuefa/law-data/releases) 发布。

状态判断依据最高人民法院历次废止、修改决定（含法释〔2020〕16号民法典配套清理清单），与官方正文交叉比对。正文以官方发布为准。

## 参与

发现错漏、状态过期、官方链接失效，欢迎开 issue 或直接 PR，见 [CONTRIBUTING.md](CONTRIBUTING.md)。不用先成为贡献者才能提问。

## 许可

- **正文**：国家机关官方文件，依《著作权法》第五条不受著作权保护，可自由复制、转载、摘编，商用无需许可；
- **整理成果**（筛选口径、效力标注、字段结构）：[CC BY 4.0](LICENSE)。署名「苏酥学法」并链接回 <https://susujuris.cn/data.html> 是请求，不是限制。

## 相关项目

- [Just Laws](https://github.com/ImCa0/just-laws)：开源中国法律文库，法律原文清晰可读；
- [苏酥学法](https://susujuris.cn/)：法经济学笔记、概念库与站内检索。
