# FBA / FBM 选品评估规则｜版本历史总表

> 本文件用于记录 FBA / FBM 选品评估规则从第一版到当前最新版的演化过程。  
> 当前默认执行版本：`v6.1`。  
> 执行栈：`v6.0 截图初筛成本闸门最终版` + `v6.1 类目退货率预设系统`。

---

## 0. 所有版本号总览

```yaml
version_history_index:
  current_latest_version: "v6.1"
  current_latest_file: "knowledge/fba-and-analysis/FBA评分体系-v6.1-类目退货率预设系统.txt"
  base_latest_file: "knowledge/fba-and-analysis/FBA评分体系.txt"
  execution_rule: "默认执行v6.1；旧版只作为历史参考"

  all_versions:
    - sequence: 1
      version: "v1.0"
      status: "archived / 已有旧版原文"
    - sequence: 2
      version: "v1.1"
      status: "archived / 已有旧版原文"
    - sequence: 3
      version: "v2.0"
      status: "archived / 已有旧版原文"
    - sequence: 4
      version: "v2.1"
      status: "archived / 已有旧版原文"
    - sequence: 5
      version: "v3.0"
      status: "archived / 已有旧版原文"
    - sequence: 6
      version: "v3.1"
      status: "archived / 已有旧版原文"
    - sequence: 7
      version: "v3.3"
      status: "archived / 已有旧版原文"
    - sequence: 8
      version: "v4.1"
      status: "archived / 已有旧版原文"
    - sequence: 9
      version: "v4.1.1"
      status: "archived / 已有旧版原文"
    - sequence: 10
      version: "v4.2"
      status: "archived / Git提交记录可确认"
    - sequence: 11
      version: "v5.0"
      status: "archived / 待补完整原文或未独立落库"
    - sequence: 12
      version: "v6.0"
      status: "archived / 当前基础版本"
    - sequence: 13
      version: "v6.1"
      status: "latest / 当前最新版 / 默认执行"
```

---

## 1. 统一记录格式

每个版本统一使用以下字段：

```yaml
version_record_format:
  sequence: "版本顺序编号"
  version: "版本号"
  title: "版本标题"
  status: "latest / archived / draft / unknown"
  source_status: "已确认原文 / Git提交记录可确认 / 待补完整原文 / 历史归纳"
  source_location: "文件路径、上传文件、Git提交记录或历史说明"
  total_weight: "权重合计"
  default_weights: "默认权重"
  execution_status: "是否作为当前执行版本"
  core_change: "本版本相对上一版的核心变化"
  notes: "补充说明"
```

---

## 2. 版本记录

### 版本 01｜v1.0

```yaml
sequence: 1
version: "v1.0"
title: "亚马逊FBA选品判断规则｜YAML基础版"
status: "archived"
source_status: "已有旧版原文"
source_location: "历史上传文件：选品逻辑.md / 相关旧版文件"
total_weight: "100%"
default_weights: "15/50/15/20"
execution_status: "不作为当前执行版本"
core_change:
  - "建立最早的YAML化选品规则"
  - "确立维度0一票否决 + 维度1-4综合评估"
  - "要求使用权重、单项达成率、加权贡献、综合达成率"
notes:
  - "该版本已经过期"
```

---

### 版本 02｜v1.1

```yaml
sequence: 2
version: "v1.1"
title: "亚马逊FBA选品判断规则｜1688截图序号增强版"
status: "archived"
source_status: "已有旧版原文"
source_location: "历史上传文件：选品逻辑2.md / 相关旧版文件"
total_weight: "100%"
default_weights: "15/50/15/20"
execution_status: "不作为当前执行版本"
core_change:
  - "新增1688候选产品字段抽取规则"
  - "要求保留1688截图原始序号"
  - "明确截图序号是溯源字段，不等于推荐排序"
notes:
  - "该版本已经过期"
```

---

### 版本 03｜v2.0

```yaml
sequence: 3
version: "v2.0"
title: "亚马逊选品综合判断规则｜校准后综合达成率版"
status: "archived"
source_status: "已有旧版原文"
source_location: "历史上传文件：选品逻辑3.md / 相关旧版文件"
total_weight: "100%"
default_weights: "15/50/15/20"
execution_status: "不作为当前执行版本"
core_change:
  - "引入原始综合达成率与校准后综合达成率"
  - "最终结论优先参考校准后综合达成率，但否决项、硬性红线、真实利润优先"
  - "形成较完整的执行顺序和输出顺序"
notes:
  - "该版本已经过期"
  - "校准后综合达成率逻辑在后续版本中被删除或弱化"
```

---

### 版本 04｜v2.1

```yaml
sequence: 4
version: "v2.1"
title: "亚马逊选品判断规则｜多表格输出版"
status: "archived"
source_status: "已有旧版原文"
source_location: "历史上传文件：选品逻辑4.md / 相关旧版文件"
total_weight: "100%"
default_weights: "15/50/15/20"
execution_status: "不作为当前执行版本"
core_change:
  - "在v2.0基础上整理为固定多表格输出结构"
  - "保留原有权重、否决项、综合达成率校准、成本模型"
  - "强调先输出百分比评估表，再输出1688推荐、否决项评价、详细分析和最终结论"
notes:
  - "该版本已经过期"
```

---

### 版本 05｜v3.0

```yaml
sequence: 5
version: "v3.0"
title: "亚马逊FBA选品综合评估规则｜品牌风险强化版"
status: "archived"
source_status: "已有旧版原文"
source_location: "历史上传文件：选品逻辑13.md / 相关旧版文件"
total_weight: "100%"
default_weights: "15/50/15/20"
execution_status: "不作为当前执行版本"
core_change:
  - "强化品牌、商标、IP、授权风险"
  - "将第三方品牌适配、Logo、原厂暗示、授权暗示作为重点检查对象"
  - "明确维度0优先级高于维度1-4"
  - "仍保留原始综合达成率与校准后综合达成率"
notes:
  - "该版本已经过期"
```

---

### 版本 06｜v3.1

```yaml
sequence: 6
version: "v3.1"
title: "亚马逊FBA选品综合评估规则｜兼容表达优化版"
status: "archived"
source_status: "已有旧版原文"
source_location: "历史上传文件：选品逻辑14.md / 相关旧版文件"
total_weight: "100%"
default_weights: "15/50/15/20"
execution_status: "不作为当前执行版本"
core_change:
  - "对 Compatible For / Fit For / Replacement For / Suitable For / Intended For 等兼容表达进行细化"
  - "不再把所有兼容表达自动等同于品牌侵权"
  - "将兼容表达放入维度0合规检查，而不是一律直接否决"
  - "要求无Logo、无原厂包装、无官方授权暗示、无仿冒外观"
notes:
  - "该版本已经过期"
```

---

### 版本 07｜v3.3

```yaml
sequence: 7
version: "v3.3"
title: "亚马逊FBA选品综合评估规则｜人读友好 + AI执行友好版"
status: "archived"
source_status: "已有旧版原文"
source_location: "历史上传文件：选品逻辑15.md / 相关旧版文件"
total_weight: "过渡版本，待以原文为准"
default_weights: "过渡版本，待以原文为准"
execution_status: "不作为当前执行版本"
core_change:
  - "将规则整理为Markdown说明 + YAML规则块"
  - "增强人读友好和AI执行友好"
  - "继续强调维度0先行、真实利润和售后全损风险"
notes:
  - "该版本已经过期"
```

---

### 版本 08｜v4.1

```yaml
sequence: 8
version: "v4.1"
title: "亚马逊FBA/FBM选品综合评估规则｜兼容表达优化最终版"
status: "archived"
source_status: "已有旧版原文"
source_location: "历史上传文件：选品逻辑16.md / Git提交记录"
total_weight: "140%"
default_weights: "21/70/21/28 或 70/21/21/28 过渡，具体以对应文件为准"
execution_status: "不作为当前执行版本"
core_change:
  - "将总权重调整为140%"
  - "强化兼容表达的可继续评估条件"
  - "禁用校准后综合达成率，强调原始综合达成率"
notes:
  - "该版本已经过期"
```

---

### 版本 09｜v4.1.1

```yaml
sequence: 9
version: "v4.1.1"
title: "亚马逊FBA/FBM选品综合评估规则｜兼容表达优化最终版"
status: "archived"
source_status: "已有旧版原文"
source_location: "历史上传文件：选品逻辑-给人读的1.md / 相关旧版文件"
total_weight: "140%"
default_weights: "70/21/21/28"
execution_status: "不作为当前执行版本"
core_change:
  - "修正v4.1中的权重表达"
  - "明确投产比权重为70%，产品属性与需求为21%，风险承受比为21%，1688匹配度为28%"
  - "强调投产比是核心优先维度"
notes:
  - "该版本已经过期"
```

---

### 版本 10｜v4.2

```yaml
sequence: 10
version: "v4.2"
title: "亚马逊FBA/FBM选品综合评估规则｜兼容表达优化 + 重量参考系统最终版"
status: "archived"
source_status: "Git提交记录可确认"
source_location: "Git提交：9c7966158b8973af83d80777a9570e0958c44297"
total_weight: "140%"
default_weights: "21/70/21/28"
execution_status: "不作为当前执行版本"
core_change:
  - "加入重量参考系统"
  - "要求计算实际重量、体积重、计费重量、跨境运费、运费占销售额比例"
  - "明确重量不是单独维度，而是影响投产比、产品属性与风险承受比的强制参考参数"
  - "增加抛货、偏重、重货、低价重货风险判断"
notes:
  - "该版本已经过期"
```

---

### 版本 11｜v5.0

```yaml
sequence: 11
version: "v5.0"
title: "亚马逊FBA/FBM选品综合评估规则｜成本闸门过渡版"
status: "archived"
source_status: "待补完整原文或未独立落库"
source_location: "历史演化占位；当前仓库未确认独立v5.0原文"
total_weight: "140%"
default_weights: "待补原文确认"
execution_status: "不作为当前执行版本"
core_change:
  - "作为 v4.2 到 v6.0 之间的编号占位"
  - "可能对应从重量参考系统向截图初筛、成本闸门、利润压力测试迁移的过渡阶段"
  - "当前未找到独立落库文本，不编造具体规则"
notes:
  - "该版本只保留编号，等待以后补充原文"
```

---

### 版本 12｜v6.0

```yaml
sequence: 12
version: "v6.0"
title: "亚马逊FBA/FBM选品综合评估规则｜截图初筛成本闸门最终版"
status: "archived_base_current"
source_status: "当前基础版本原文"
source_location: "knowledge/fba-and-analysis/FBA评分体系.txt"
total_weight: "140%"
default_weights: "70/21/21/28"
execution_status: "作为v6.1的基础版本，不单独作为最新默认执行版本"
core_change:
  - "改为截图初筛优先"
  - "一张Amazon截图 + 一张1688截图即可进行初筛"
  - "加入成本极致保守、利润闸门、采购单位换算、默认计费重量、三重压力测试、成本可信度"
  - "要求数据缺失时必须使用保守默认值继续计算，不因重量、包装、采购单位缺失而停止"
  - "利润闸门优先级高于原始综合达成率"
notes:
  - "该版本是当前基础版本"
  - "已被v6.1继承并扩展"
```

---

### 版本 13｜v6.1

```yaml
sequence: 13
version: "v6.1"
title: "亚马逊FBA/FBM选品综合评估规则｜类目退货率预设系统补充版"
status: "latest"
source_status: "当前仓库最新原文"
source_location: "knowledge/fba-and-analysis/FBA评分体系-v6.1-类目退货率预设系统.txt"
total_weight: "140%"
default_weights: "70/21/21/28"
execution_status: "当前唯一默认执行版本"
core_change:
  - "继承v6.0截图初筛成本闸门最终版"
  - "新增类目退货率预设系统"
  - "将Amazon产品类目作为默认退货率和售后全损预留来源之一"
  - "低退货率类目可以适度提高维度1投产比单项达成率"
  - "高退货率类目必须提高售后全损预留，并降低维度1投产比单项达成率"
  - "新增Subscribe & Save、Office Products、Health & Household、Beauty & Personal Care、Arts/Crafts/Sewing、Pet Supplies、Toys & Games、Patio/Lawn/Garden、Home & Kitchen、Kitchen & Dining、Baby、Musical Instruments、Sports & Outdoors、Clothing/Shoes/Jewelry等类目默认退货率"
notes:
  - "这是当前最新版"
  - "以后未特别声明使用旧版时，一律执行本版本"
```

---

## 3. 当前执行规则

```yaml
current_execution_policy:
  default_version: "v6.1"
  default_file: "knowledge/fba-and-analysis/FBA评分体系-v6.1-类目退货率预设系统.txt"
  base_file: "knowledge/fba-and-analysis/FBA评分体系.txt"
  execution_stack:
    - "v6.0 截图初筛成本闸门最终版"
    - "v6.1 类目退货率预设系统"
  old_versions_usage: "只做历史参考，不做默认执行"
  if_conflict: "以v6.1新增模块为准，但不改变v6.0核心流程和权重"
  if_user_explicitly_requests_old_version: "可以按指定旧版本分析，但必须注明旧版已过期"
```

---

## 4. 后续维护规则

```yaml
maintenance_rules:
  - "新增版本时，必须先在本文件最前面的 all_versions 中追加版本号"
  - "再按统一记录格式新增一个版本段落"
  - "每个版本必须有 sequence、version、title、status、source_status、source_location、total_weight、default_weights、execution_status、core_change、notes"
  - "如果没有完整原文，必须写待补完整原文，不能伪造"
  - "只有明确标记为 latest 的版本可以作为默认执行版本"
  - "修改主版本时，不直接覆盖旧主版本，必须创建带版本号的新版本文件"
  - "新增主版本后，必须同步更新 LATEST.md 和 VERSION_HISTORY.md"
```
