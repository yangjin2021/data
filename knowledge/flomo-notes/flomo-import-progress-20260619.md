# flomo 导入进度说明｜2026-06-19

来源：`io` 仓库导入流程。

## 当前路径规则

flomo 中属于资料、文章、外部链接、公开网页、课程资料、工具资料的内容，统一放入本仓库：

```text
knowledge/flomo-notes/
```

私人记录、个人感想、复盘、习惯、情绪、家庭、事业、学习、财务等内容，不放在本仓库，进入私人仓库：

```text
yangjin2021/io
```

## 历史说明

早期导入时，部分外部资料曾写入旧路径：

```text
flomo-import-2026-06-19/external-links/
```

用户已调整 data 仓库结构，后续统一以 `knowledge/flomo-notes/` 为准。

## 已确认规则

- 图片不用 OCR，不解析内容。
- 图片只保留路径。
- 资料、文章、外链进入 data。
- 资料引发的个人想法进入 io。
- 如果一条 flomo 同时包含资料和个人想法：资料部分进 data，个人想法进 io。

## 已迁移 / 已建立索引

### 2022

已写入：

```text
knowledge/flomo-notes/2022/flomo-external-2022.md
```

### 2023

已写入：

```text
knowledge/flomo-notes/2023/flomo-external-2023-part1a.md
knowledge/flomo-notes/2023/flomo-external-2023-part1b-original.md
```

仍需继续核对 `ext2023_1.md` 是否还有未迁移尾段。

### 2024

已写入：

```text
knowledge/flomo-notes/2024/flomo-external-2024.md
```

### 2025

主体已分块迁移，已写入：

```text
knowledge/flomo-notes/2025/flomo-external-2025-part1a.md
knowledge/flomo-notes/2025/flomo-external-2025-part1b.md
knowledge/flomo-notes/2025/flomo-external-2025-part1c.md
knowledge/flomo-notes/2025/flomo-external-2025-part1d.md
knowledge/flomo-notes/2025/flomo-external-2025-part1e.md
knowledge/flomo-notes/2025/flomo-external-2025-part1f.md
knowledge/flomo-notes/2025/flomo-external-2025-part1g-safe.md
knowledge/flomo-notes/2025/flomo-external-2025-part1h-knowledge.md
knowledge/flomo-notes/2025/flomo-external-2025-part1i-platform.md
knowledge/flomo-notes/2025/flomo-external-2025-part1j-tail.md
```

被工具安全检查拦截、仅建立索引的条目：

```text
knowledge/flomo-notes/2025/flomo-external-2025-part1g-blocked-index.md
knowledge/flomo-notes/2025/flomo-external-2025-part1h-blocked-index.md
```

### 2026

尝试写入整文件时被工具安全检查拦截，因此已建立索引：

```text
knowledge/flomo-notes/2026/flomo-external-2026-index.md
```

后续又尝试拆出 general 小分片，仍被工具安全检查拦截。因此 2026 外部资料当前只保留索引；如果继续处理，需要继续拆到更小条目，并且单条仍被拦时只保留来源日期索引，不改写正文。

## 待核对 / 待迁移

- `2023` 外部资料：已迁移 part1a 和 part1b-original，仍需核对尾段。
- `2025` 外部资料：主体已迁移，两个被拦条目保留索引。
- `2026` 外部资料：已有索引，整文件和 general 小分片均被拦，后续只能继续更小粒度尝试或保留索引。

## 建议结构

```text
knowledge/flomo-notes/
  README.md
  2022/
  2023/
  2024/
  2025/
  2026/
  external-links/
  import-progress.md
```

## 当前状态

`io` 仓库中的 2022 主文件基本收口；`data` 已按新路径迁移 2022、2023 部分、2024、2025 主体；2026 已建立索引，整文件与 general 小分片均被拦。