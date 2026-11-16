# LLM Wiki · 大模型知识库

> 面向中文开发者的大模型 / 多模态学习笔记仓库。
> 每篇文章都是可独立阅读的深度长文：**原理拆解 + 自绘架构图 + 视频原帧对照 + 可落地清单**。
> 文章之间共享同一套"多模态四步地图"与"知识运行时"框架，可单独读，也可按路径连读。

---

## 📚 文章目录

| # | 文章 | 主题 | 关键词 | 状态 |
|---|---|---|---|---|
| 01 | [多模态原理：从声波到语义，一台 AI 如何"听懂"你说话](articles/01-multimodal-principles.md) | 多模态 / 语音识别 | Fun-ASR、Paraformer、梅尔谱、CIF/CTC、LLM-ASR、GRPO | ✅ 完成 |
| 02 | [LLM Wiki 深度解析：从 RAG、GraphRAG 到大模型知识运行时](articles/02-llm-wiki.md) | 知识运行时 | RAG、GraphRAG、摄取编译、知识治理、生命周期 | ✅ 完成 |

> 规划中：多模态视觉篇（ViT 与图文对齐）、Audio-LLM 评测篇、Agent 记忆篇。欢迎提 Issue 建议选题。

---

## 🗺️ 推荐阅读路径

- **路线 A：想搞懂"大模型如何理解世界"**
  01 多模态原理（语音是最小切口）→ 图 1 的四步地图 → 回看 02 的"知识运行时"，理解"一次编译、长期复用"与"一次对齐、跨模态复用"是同一思想在不同层面的投影。
- **路线 B：想解决"知识永远在丢"**
  02 LLM Wiki（RAG 的痛点与解法）→ 01 中的"检索/对齐"章节 → 组合出"语音入库 → 结构化沉淀"的完整管线。
- **路线 C：只想快速落地一个功能**
  直接跳到各篇的「动手」与「尽职调查清单」章节。

---

## 🖼️ 配图与目录约定

```
articles/               # 每篇文章一个 md（NN-<slug>.md）
  _template.md          # 新文章模板
images/                 # 历史文章配图（根目录，兼容已发布文章的 jsDelivr 直链）
  multimodal/           # 文章 01 的配图：NN-fig-*（自绘）与 NN-k*（视频原帧）
```

- 正文中的图片一律使用**相对路径**（GitHub 直接可渲染）；
- 掘金 / 公众号发文时，把相对路径批量替换为 jsDelivr 直链即可；
- 新文章：图片放 `images/<文章 slug>/`，正文写 `../images/<文章 slug>/NN-xxx.png`。

---

## ✍️ 新增一篇文章的流程

1. 复制 `articles/_template.md` → `articles/NN-<slug>.md`；
2. 在 `images/<slug>/` 放配图：自绘图编号 `NN-fig-*.png`（2000px 宽、白底），视频/截图编号 `NN-k*.jpg`；
3. 更新本 README 的「文章目录」表；
4. 提交：`git add -A && git commit -m "docs: add NN-<slug>" && git push`。

## 📌 直链格式（jsDelivr 加速）

```
https://cdn.jsdelivr.net/gh/MingNingJian/demo-llm-wiki@main/<相对路径>
# 例：
https://cdn.jsdelivr.net/gh/MingNingJian/demo-llm-wiki@main/images/multimodal/01-fig-01-multimodal-stack.png
```

备用线路：raw.githack.com / cdn.statically.io（用法相同，替换域名即可）。

---

## ⚠️ 版权与免责

- 文中**视频原帧**仅用于学习对照，版权归原作者（B 站 UP 主「乐茵linn」）所有；
- 模型效果数字均来自官方论文 / README 公开表格，具体复现口径以官方为准；
- 本文档是个人学习笔记，不代表任何官方立场。

## 📄 License

文章内容采用 [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/) 共享；代码片段可自由使用。
