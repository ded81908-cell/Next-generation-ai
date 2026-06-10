# Data Flow

## フロー

User Input
↓
Planner
↓
Task DAG生成
↓
Execution Engine
↓
Memory保存
↓
Evaluation
↓
Improvement
↓
次のタスク

---

## データタイプ

- task
- result
- memory
- metrics

---

## 更新タイミング

- 各stepで保存
- loop終了時に集約

---

## イベント駆動

event = {
  "type": "",
  "payload": {}
}

trigger(event)