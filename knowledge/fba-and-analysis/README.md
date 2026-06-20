# FBA And Analysis

用于保存亚马逊选品判断、FBA/FBM 成本测算、1688货源匹配和通用分析方法。

---

## 当前最新规则

```yaml
framework_index:
  framework_name: "亚马逊FBA/FBM选品综合评估规则"
  current_latest_version: "7.1"
  current_latest_file: "FBA评分体系-v7.1-属性趋势优先版.txt"
  current_latest_title: "属性趋势优先版"
  current_latest_path: "knowledge/fba-and-analysis/FBA评分体系-v7.1-属性趋势优先版.txt"
  selection_rule: "每次分析前先读取README，再读取current_latest_file"
```

---

## 使用规则

- 每次使用“亚马逊分析框架 / FBA评分体系 / 选品分析规则”时，必须先读本 README。
- 只以 `current_latest_file` 指向的文件为当前有效规则。
- 不要根据文件名猜测最新版本。
- 旧版本只作为历史参考。

---

## 更新规则

新增版本时：

1. 新建独立版本文件，不覆盖旧文件。
2. 文件名格式：`FBA评分体系-v版本号-简短标题.txt`。
3. 更新 README 中的 `current_latest_version`、`current_latest_file`、`current_latest_path`。
4. 在版本历史中追加记录。

---

## 版本历史

| 版本 | 文件 | 说明 |
|---|---|---|
| v7.1 | `FBA评分体系-v7.1-属性趋势优先版.txt` | 当前版本。产品属性与趋势为维度1，真实利润与投产比为维度2；先查产品基础属性、趋势、季节性和多平台需求，再分析利润。 |
| v7.0 | `FBA评分体系-v7.0-核心数据输出版.txt` | 核心数据输出版；去掉“维度0”，改为“否决项”；只保留两维评分和1688货源分析表。 |
| v6.0 | `FBA评分体系.txt` | 截图初筛成本闸门最终版；用保守默认值初筛成本、利润、采购单位、重量、履约和售后。 |

---

## 文件说明

- `README.md`：本目录索引文件。
- `FBA评分体系-v7.1-属性趋势优先版.txt`：当前最新规则。
- `FBA评分体系-v7.0-核心数据输出版.txt`：历史版本。
- `FBA评分体系.txt`：历史版本。
- `纵横分析法.md`：横向对比与纵向拆解方法。

---

## AI执行提示

当用户说：

- “用亚马逊分析框架分析”
- “按FBA评分体系看一下”
- “按我的选品规则分析”
- “帮我看这个Amazon产品和1688货源”
- “更新亚马逊分析框架”

必须执行：

```yaml
before_analysis:
  - "读取 knowledge/fba-and-analysis/README.md"
  - "读取 README 中 current_latest_file 指向的文件"
  - "以该文件作为唯一有效分析框架"

before_update:
  - "读取 README"
  - "新建版本文件，不覆盖旧版本"
  - "更新 README 最新版本指针"
  - "追加版本历史"
```
