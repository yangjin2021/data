# FBA / FBM 选品评估规则｜版本历史总表

> 本文件用于记录 FBA / FBM 选品评估规则从第一版到当前最新版的演化过程。  
> 当前唯一默认执行版本仍然是：`knowledge/fba-and-analysis/FBA评分体系.txt`，版本号 `v6.0`。

---

## 0. 所有版本号总览

```yaml
version_history_index:
  current_latest_version: "v6.0"
  current_latest_file: "knowledge/fba-and-analysis/FBA评分体系.txt"
  execution_rule: "默认只执行最新版；旧版只作为历史参考"

  all_versions:
    - sequence: 1
      version: "v1.0"
      status: "archived / 待补完整原文"
    - sequence: 2
      version: "v2.0"
      status: "archived / 待补完整原文"
    - sequence: 3
      version: "v3.0"
      status: "archived / 已有旧版原文"
    - sequence: 4
      version: "v3.1"
      status: "archived / 待补完整原文"
    - sequence: 5
      version: "v4.1"
      status: "archived / Git提交记录可确认"
    - sequence: 6
      version: "v4.2"
      status: "archived / Git提交记录可确认"
    - sequence: 7
      version: "v5.0"
      status: "archived / 待补完整原文或未独立落库"
    - sequence: 8
      version: "v6.0"
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
title: "亚马逊FBA选品综合评估规则｜基础版"
status: "archived"
source_status: "待补完整原文"
source_location: "历史聊天与规则演化记录"
total_weight: "100%"
default_weights: "历史早期权重，待补原文确认"
execution_status: "不作为当前执行版本"
core_change:
  - "建立基础选品评分框架"
  - "形成维度0否决项 + 维度1-4综合评估的基本结构"
  - "开始区分账号安全、投产比、产品属性、风险承受比、1688匹配度"
notes:
  - "该版本是第一版框架，后续所有版本都在此基础上迭代"
  - "完整原文未在当前仓库中确认，保留编号和历史位置"
```

---

### 版本 02｜v2.0

```yaml
sequence: 2
version: "v2.0"
title: "亚马逊FBA选品综合评估规则｜维度调整版"
status: "archived"
source_status: "待补完整原文"
source_location: "历史聊天与规则演化记录"
total_weight: "100%"
default_weights: "历史过渡权重，待补原文确认"
execution_status: "不作为当前执行版本"
core_change:
  - "对四个评估维度的顺序和权重进行调整"
  - "强化投产比、售后全损、合作伙伴佣金等成本意识"
  - "开始弱化单纯看需求和销量的判断方式"
notes:
  - "该版本属于从基础框架向保守利润模型过渡的版本"
  - "完整原文未在当前仓库中确认，保留编号和历史位置"
```

---

### 版本 03｜v3.0

```yaml
sequence: 3
version: "v3.0"
title: "亚马逊FBA选品综合评估规则｜品牌风险强化版"
status: "archived"
source_status: "已有旧版原文"
source_location: "上传文件：选品逻辑13.md"
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
  - "该版本中的100%权重、15/50/15/20权重和校准后综合达成率，均不再作为最新版执行规则"
```

---

### 版本 04｜v3.1

```yaml
sequence: 4
version: "v3.1"
title: "亚马逊FBA/FBM选品综合评估规则｜兼容表达优化版"
status: "archived"
source_status: "待补完整原文"
source_location: "历史聊天与规则演化记录"
total_weight: "100% 或过渡状态，待补原文确认"
default_weights: "历史过渡权重，待补原文确认"
execution_status: "不作为当前执行版本"
core_change:
  - "对 Compatible For / Fit For / Replacement For / Suitable For / Intended For 等兼容表达进行细化"
  - "不再把所有兼容表达自动等同于品牌侵权"
  - "将兼容表达放入维度0合规检查，而不是一律直接否决"
  - "同时要求无Logo、无原厂包装、无官方授权暗示、无仿冒外观"
notes:
  - "该版本已经过期"
  - "兼容表达思想被后续 v4.x 和 v6.0 吸收，但具体执行以 v6.0 为准"
```

---

### 版本 05｜v4.1

```yaml
sequence: 5
version: "v4.1"
title: "亚马逊FBA/FBM选品综合评估规则｜兼容表达优化最终版"
status: "archived"
source_status: "Git提交记录可确认"
source_location: "Git提交记录：v4.1 -> v4.2 的差异中可见旧标题与旧版本号"
total_weight: "140%"
default_weights: "70/21/21/28"
execution_status: "不作为当前执行版本"
core_change:
  - "将总权重调整为140%"
  - "强化兼容表达的可继续评估条件"
  - "删除或弱化校准后综合达成率逻辑，强调原始综合达成率"
  - "继续保留维度0优先、真实利润、售后全损风险的优先级"
notes:
  - "该版本已经过期"
  - "后续被 v4.2 的重量参考系统替代"
```

---

### 版本 06｜v4.2

```yaml
sequence: 6
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
  - "重量系统思想被 v6.0 吸收，但 v6.0 改为截图初筛成本闸门模型"
```

---

### 版本 07｜v5.0

```yaml
sequence: 7
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
  - "如果后续找到 v5.0 原文，应补充本段"
```

---

### 版本 08｜v6.0

```yaml
sequence: 8
version: "v6.0"
title: "亚马逊FBA/FBM选品综合评估规则｜截图初筛成本闸门最终版"
status: "latest"
source_status: "当前仓库最新原文"
source_location: "knowledge/fba-and-analysis/FBA评分体系.txt"
total_weight: "140%"
default_weights: "70/21/21/28"
execution_status: "当前唯一默认执行版本"
core_change:
  - "改为截图初筛优先"
  - "一张Amazon截图 + 一张1688截图即可进行初筛"
  - "加入成本极致保守、利润闸门、采购单位换算、默认计费重量、三重压力测试、成本可信度"
  - "要求数据缺失时必须使用保守默认值继续计算，不因重量、包装、采购单位缺失而停止"
  - "利润闸门优先级高于原始综合达成率"
notes:
  - "这是当前最新版"
  - "以后未特别声明使用旧版时，一律执行本版本"
```

---

## 3. 当前执行规则

```yaml
current_execution_policy:
  default_version: "v6.0"
  default_file: "knowledge/fba-and-analysis/FBA评分体系.txt"
  old_versions_usage: "只做历史参考，不做默认执行"
  if_conflict: "以v6.0为准"
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
```
