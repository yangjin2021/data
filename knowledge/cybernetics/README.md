# Cybernetics Complete Library

这个分支把控制论相关资料按资料性质重新编排，保留一份去重后的主资料库。

## 目录结构

| 目录 | 资料性质 | 内容 |
|---|---|---|
| `00-overview-总纲索引/` | 总纲与导航 | 总体大纲、知识图谱、书本总结、理论概念总览、大一统总纲 |
| `01-original-pdfs-PDF原件/` | 原始书籍扫描件 | 34 本控制论相关 PDF 原件和 PDF 说明 |
| `02-book-notes-书籍笔记/` | 每本书的整理笔记 | 34 本书的结构化 Markdown 笔记 |
| `03-ocr-fulltext-OCR全文/` | 可检索全文 | 34 本书的 OCR 全文 Markdown |
| `04-ocr-page-data-OCR页数据/` | 页级 OCR 数据 | 34 本书逐页 OCR JSONL 数据 |
| `05-concept-cards-概念卡片/` | 概念知识卡 | 40 个控制论、系统论、信息论、最优控制相关概念 |
| `06-metadata-元数据/` | 数据清单与生成信息 | `manifest.json`、OCR 上传/生成信息 |
| `07-obsidian-config-Obsidian配置/` | Obsidian 配置 | 原 vault 的配置文件 |
| `90-cross-domain-references-跨域参考/` | 跨域参考资料 | 指向 FBA 评分体系、纵横分析法的 canonical 位置 |

## 快速入口

- 总纲：`00-overview-总纲索引/控制论大一统总纲.md`
- 总体大纲：`00-overview-总纲索引/总体大纲.md`
- 书本总结：`00-overview-总纲索引/控制论书本总结.md`
- 核心理论：`00-overview-总纲索引/核心理论与概念.md`
- 知识图谱：`00-overview-总纲索引/知识图谱.md`
- 完整目录：`CYBERNETICS_LIBRARY.md`

## 整理原则

- 按资料性质分层，而不是按来源分层。
- PDF、OCR 全文、OCR 页数据、书籍笔记、概念卡片分开放置。
- `90-cross-domain-references-跨域参考/` 只保留跨域引用说明，正文放在对应主题目录。
- 重复快照已删除；当前分支保留一份 canonical copy。
