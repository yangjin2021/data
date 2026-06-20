# FBA / FBM 选品规则｜版本管理约定

> 本文件用于约束以后修改 `knowledge/fba-and-analysis/` 下 FBA / FBM 选品规则时的版本管理方式。

---

## 1. 核心原则

以后修改主版本时，不直接覆盖旧主版本，而是创建一个带版本号的新版本文件。

```yaml
versioning_policy:
  rule: "主版本修改必须生成新版本文件，不直接覆盖旧版本"
  directory: "knowledge/fba-and-analysis/"
  current_latest_pointer: "LATEST.md"
  version_history_file: "VERSION_HISTORY.md"
  current_rule_file: "FBA评分体系.txt"
```

---

## 2. 新版本文件命名规则

新增主版本时，使用明确版本号命名。

推荐格式：

```text
FBA评分体系-v6.1.txt
FBA评分体系-v7.0.txt
FBA评分体系-v7.1.txt
```

也可以根据内容增加简短说明：

```text
FBA评分体系-v6.1-利润闸门优化版.txt
FBA评分体系-v7.0-截图初筛新版.txt
```

---

## 3. 修改流程

```yaml
main_version_update_flow:
  step_1: "读取当前最新版"
  step_2: "根据修改内容确定新版本号"
  step_3: "创建新的带版本号文件，例如 FBA评分体系-v6.1.txt"
  step_4: "更新 VERSION_HISTORY.md，把新版本加入版本总览和版本记录"
  step_5: "更新 LATEST.md，把最新版指向新版本文件"
  step_6: "如仍保留 FBA评分体系.txt 作为入口文件，则只用于指向当前最新版或同步当前最新版内容"
```

---

## 4. 不允许的操作

```yaml
forbidden_operations:
  - "直接覆盖旧版本，导致历史版本丢失"
  - "只修改 FBA评分体系.txt，但不增加新版本号"
  - "新增版本后不更新 VERSION_HISTORY.md"
  - "新增版本后不更新 LATEST.md"
  - "把草稿、过渡版本、未确认版本标记为 latest"
```

---

## 5. 版本号建议

```yaml
version_numbering:
  patch_update:
    example: "v6.0 -> v6.1"
    use_when:
      - "小幅规则优化"
      - "措辞修正"
      - "局部成本项补充"
      - "输出格式小调整"

  minor_update:
    example: "v6.0 -> v6.5"
    use_when:
      - "新增一个重要模块"
      - "调整部分执行流程"
      - "新增一种评估场景"

  major_update:
    example: "v6.0 -> v7.0"
    use_when:
      - "核心逻辑变化"
      - "权重体系变化"
      - "执行顺序变化"
      - "从一个主框架升级到另一个主框架"
```

---

## 6. 当前约定

```yaml
current_agreement:
  user_instruction: "以后在修改主版本的时候，直接给一个加上版本号的新版本"
  implementation: "以后主版本修改采用新建版本文件 + 更新LATEST + 更新VERSION_HISTORY的方式"
  default_latest_before_next_update: "v6.0"
```
