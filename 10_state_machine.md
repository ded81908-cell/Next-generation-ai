# State Machine Specification

## 目的
システムの全状態遷移を定義する

---

## 状態一覧

INITIAL
IDLE
PLANNING
EXECUTING
WAITING
EVALUATING
LEARNING
IMPROVING
ERROR
TERMINATED

---

## 状態遷移

INITIAL → IDLE

IDLE → PLANNING
条件：
- タスクが存在する

PLANNING → EXECUTING
条件：
- タスク分解完了

EXECUTING → WAITING
条件：
- 外部依存あり（APIなど）

EXECUTING → EVALUATING
条件：
- 実行完了

WAITING → EXECUTING
条件：
- 応答受信

EVALUATING → LEARNING

LEARNING → IMPROVING

IMPROVING → IDLE

任意状態 → ERROR
条件：
- 例外発生

ERROR → IDLE
条件：
- recovery成功

---

## 状態データ

state = {
  "current": "",
  "previous": "",
  "iteration": int,
  "error_count": int
}

---

## 要件

- 状態は必ず保存
- 各遷移はログに記録