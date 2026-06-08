# Execution Engine

## 目的
タスク実行処理の中核

---

## フロー

1. task取得
2. executor選択
3. 実行
4. 結果保存
5. 次タスク

---

## 実行関数

execute(task):

    validate(task)

    agent = select_executor(task)

    result = agent.run(task)

    store(result)

    return result

---

## バリデーション

- 必須フィールド確認
- 依存チェック

---

## retry

max_retry = 3

if fail:
    retry++