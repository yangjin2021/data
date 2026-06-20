# FBA/FBM 选品评估规则｜最新版本指针

## 最新版本

当前最新、唯一默认执行版本：

- 最新版本号：`version: "6.1"`
- 最新版本文件：`knowledge/fba-and-analysis/FBA评分体系-v6.1-类目退货率预设系统.txt`
- 基础版本文件：`knowledge/fba-and-analysis/FBA评分体系.txt`
- 基础版本号：`version: "6.0"`
- 标题：`亚马逊FBA/FBM选品综合评估规则｜类目退货率预设系统补充版`
- 模式：`截图初筛优先 / 成本极致保守 / 利润闸门优先 / 账号安全优先 / 类目退货率参与投产比`
- 权重合计：`140%`
- 默认权重：`70/21/21/28`

## 执行规则

1. 以后做亚马逊 FBA / FBM 选品分析时，默认执行 `v6.1`。
2. `v6.1` 的执行方式为：`v6.0 截图初筛成本闸门规则` + `v6.1 类目退货率预设系统`。
3. `v6.1` 不推翻 `v6.0` 的核心流程、维度和权重，只新增“类目退货率作为维度1投产比的默认来源之一”。
4. 其他聊天记录、上传文件、旧版规则、历史草稿，只能作为历史参考，不作为当前执行版本。
5. 如果旧文件中出现 `version: "1.0"`、`2.0`、`2.1`、`3.0`、`3.1`、`3.3`、`4.1`、`4.1.1`、`4.2`、`5.0`、`15/50/15/20`、`100%`、`校准后综合达成率` 等内容，默认视为过期规则。
6. 若用户没有特别声明“使用旧版”，一律执行 `version: "6.1"`。
7. 以后修改主版本时，不直接覆盖旧版本，而是新建带版本号的新版本文件，并同步更新本文件和 `VERSION_HISTORY.md`。

## 当前执行优先级

```yaml
latest_rule_source:
  repository: "yangjin2021/data"
  branch: "main"
  latest_version: "6.1"
  latest_version_file: "knowledge/fba-and-analysis/FBA评分体系-v6.1-类目退货率预设系统.txt"
  base_version: "6.0"
  base_file: "knowledge/fba-and-analysis/FBA评分体系.txt"
  status: "latest"
  priority: "highest"

execution_stack:
  - "v6.0 截图初筛成本闸门最终版"
  - "v6.1 类目退货率预设系统"

outdated_sources:
  - "选品逻辑.md"
  - "选品逻辑1-16.md 等历史上传文件"
  - "历史聊天记录中的旧版FBA规则"
  - "version 1.x / 2.x / 3.x / 4.x / 5.x 等旧版规则"
  - "权重合计100%的旧规则"
  - "15/50/15/20 等旧权重规则"
```
