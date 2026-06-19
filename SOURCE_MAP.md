# Source Map

本文件记录 `data` 仓库 main 分支的资料来源和当前 canonical 位置。2026-06-19 之后，资料按主题进入 `knowledge/`，不再按旧仓库名、旧分支名或临时导入目录保存。

## Canonical Areas

| Current path | Main content | Source notes |
|---|---|---|
| `knowledge/business-theory/` | 商业模型、分析流程、报告模板、速查表 | 由 main 上新增的 business theory 文件整理保留 |
| `knowledge/fba-and-analysis/` | FBA 评分体系、纵横分析法 | 从删除前 main 恢复最新版；早期 `think-model` 只作为历史来源 |
| `knowledge/cybernetics/` | 控制论完整资料库：PDF、书籍笔记、OCR、概念卡、元数据 | 原 `cybernetics-complete-library` 分支提升为 canonical |
| `knowledge/life-50-books/` | 50 本书合法资源索引、书目数据、版权说明 | 原 `life50books/life50books` 内容提升为 canonical |
| `knowledge/flomo-notes/` | flomo external links 分年度资料 | 合并 main 与 `flomo-import-2026-06-19` 归档里的 external-links |
| `knowledge/trading-and-python-data/` | 交易策略、Python 环境、字体/依赖资源、工具脚本 | 原 `data-private/master` 与交易策略分支内容整理为主题目录 |

## Removed Wrappers

这些目录不再作为 main 的正式结构保留：

- `branch-archives/`：旧分支整份快照。可用内容已经提升到 `knowledge/`；重复和旧导入壳已删除。
- `flomo-import-2026-06-19/`：临时导入壳。外部链接已移动到 `knowledge/flomo-notes/external-links/`。
- `docs/source-metadata/`：旧迁移说明壳。当前来源说明集中到本文件。
- `knowledge/cybernetics-pdfs/`、`knowledge/cybernetics-ocr-vault/`：旧控制论拆分目录。当前统一由 `knowledge/cybernetics/` 管理。

## Historical Branches

远端分支已在此前清理为仅保留 `main`。旧分支内容的处理结果：

| Historical branch | Current result |
|---|---|
| `cybernetics-complete-library` | Promoted to `knowledge/cybernetics/` |
| `life50books` | Promoted to `knowledge/life-50-books/` |
| `flomo-import-2026-06-19` | External links merged into `knowledge/flomo-notes/` |
| `think-model` | Superseded by latest restored `knowledge/fba-and-analysis/` |
| `trading-python-strategy-notes` | Deduplicated against `knowledge/trading-and-python-data/` |

## Duplicate Policy

- Canonical topic folders keep the readable working copy.
- Historical whole-branch snapshots are not kept in main.
- Cross-topic references should use README links instead of copying the same FBA or analysis file into multiple folders.
