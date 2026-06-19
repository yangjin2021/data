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

## 待核对

- 是否需要把旧路径 `flomo-import-2026-06-19/external-links/` 下的文件迁移到本目录。
- 是否需要按年份拆分为：
  - `2022/`
  - `2023/`
  - `2024/`
  - `2025/`
  - `2026/`
- 是否需要按主题拆分为：
  - `business/`
  - `learning/`
  - `psychology/`
  - `trading/`
  - `tools/`
  - `external-links/`

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

`io` 仓库中的 2022 主文件基本收口；2023、2024 已导入大量分类，后续主要做零散核对与旧路径迁移。
