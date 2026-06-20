# FBA And Analysis

这里保存亚马逊选品判断、FBA/FBM 成本测算、1688货源匹配和通用分析方法。

---

# 使用规则｜必须先读最新版本

以后每次使用“亚马逊分析框架 / FBA评分体系 / 选品分析规则”时，必须先读取本 README，并以本 README 指定的 `current_latest_file` 为准。

如果目录中存在多个版本文件，不要默认读取旧文件，也不要仅凭文件名猜测最新版本。必须以本 README 的最新版本指针为准。

```yaml
framework_index:
  framework_name: "亚马逊FBA/FBM选品综合评估规则"
  current_latest_version: "6.0"
  current_latest_file: "FBA评分体系.txt"
  current_latest_title: "截图初筛成本闸门最终版"
  current_latest_path: "knowledge/fba-and-analysis/FBA评分体系.txt"
  selection_rule: "每次分析前先读取README，再读取current_latest_file"
```

---

# 更新规则｜以后新增版本，不覆盖旧版本

以后当用户要求“更新亚马逊分析框架的新版本”时，执行以下规则：

```yaml
version_update_rule:
  do:
    - "新增一个独立的新版本文件"
    - "新版本文件名使用：FBA评分体系-v版本号-简短标题.txt"
    - "更新本README中的current_latest_version"
    - "更新本README中的current_latest_file"
    - "在version_history中追加新版本记录"
    - "以后分析时优先读取README指向的最新版本"

  do_not:
    - "不要覆盖旧版本文件"
    - "不要删除旧版本文件"
    - "不要只凭文件名猜测最新版本"
    - "不要在未更新README的情况下新增版本"

  legacy_file_rule:
    - "FBA评分体系.txt 当前作为 v6.0 最新版本文件使用"
    - "以后如新增 v6.1、v7.0 等版本，应新建独立文件，例如 FBA评分体系-v6.1-xxx.txt"
    - "README 的 current_latest_file 必须指向真正最新版本"
```

---

# 当前最新版本

| 项目 | 内容 |
|---|---|
| 当前最新版本 | v6.0 |
| 当前最新文件 | `FBA评分体系.txt` |
| 当前最新标题 | 截图初筛成本闸门最终版 |
| 当前最新路径 | `knowledge/fba-and-analysis/FBA评分体系.txt` |
| 使用方式 | 每次分析前先读本 README，再读当前最新文件 |

---

# 版本历史

| 版本 | 文件 | 说明 |
|---|---|---|
| v6.0 | `FBA评分体系.txt` | 截图初筛成本闸门最终版；支持一张Amazon截图 + 一张1688截图，用保守默认值直接初筛成本、利润、采购单位、重量、履约模式、售后和利润闸门。 |

---

# 文件说明

- `README.md`：本目录索引文件。每次使用分析框架前必须先读它。
- `FBA评分体系.txt`：当前最新 v6.0 分析框架文件。
- `纵横分析法.md`：横向对比与纵向拆解的分析方法。

---

# 给AI的强制执行提示

当用户说：

- “用亚马逊分析框架分析”
- “按FBA评分体系看一下”
- “按我的选品规则分析”
- “帮我看这个Amazon产品和1688货源”
- “更新亚马逊分析框架”

必须执行：

```yaml
ai_execution_instruction:
  before_analysis:
    - "读取 knowledge/fba-and-analysis/README.md"
    - "从README中识别current_latest_file"
    - "读取current_latest_file作为唯一有效分析框架"

  before_update:
    - "读取 knowledge/fba-and-analysis/README.md"
    - "不要直接覆盖旧版本"
    - "创建新版本文件"
    - "更新README的current_latest_version和current_latest_file"
    - "追加version_history"

  priority:
    - "README中的current_latest_file优先级最高"
    - "旧版本文件只作为历史参考"
```
