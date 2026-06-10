# Memory System

## データ構造

memory = {
  "short": [],
  "history": [],
  "knowledge": []
}

---

## 操作

save(entry)
load(query)
search(vector)

---

## 圧縮

if size > threshold:
    summarize()

---

## エントリ形式

{
  "task": "",
  "result": "",
  "score": "",
  "agent": "",
  "timestamp": ""
}