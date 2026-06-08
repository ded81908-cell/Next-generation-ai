# Task Graph (DAG)

## 目的
タスク依存関係の管理

---

## ノード構造

task = {
  "id": "",
  "description": "",
  "status": "pending | running | done | failed",
  "dependencies": [],
  "priority": int
}

---

## DAGルール

- 循環禁止
- dependency完了後のみ実行

---

## 実行条件

if all(dependency.status == "done"):
    executable = True

---

## キュー

ready_queue = []
waiting_queue = []

---

## 更新

- 完了時：dependentsをqueueに移動