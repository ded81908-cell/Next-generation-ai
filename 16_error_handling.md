# Error Handling

## 種類

- execution_error
- logic_error
- timeout
- invalid_output

---

## 処理

retry()
fallback()
switch_model()

---

## 例

if timeout:
    retry()

if invalid:
    replan()