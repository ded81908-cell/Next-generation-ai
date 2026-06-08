# Concurrency System

## モデル

- async execution
- task queue

---

## キュー

task_queue = []
running_tasks = []

---

## 実行

for task in ready_queue:
    run_async(task)

---

## 同期

- lock memory
- avoid race condition