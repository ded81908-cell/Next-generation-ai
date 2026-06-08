# Tool Interface Specification

## 目的
AIの「手足」を定義する

---

## ツールカテゴリ

### 1. Web
- search(query)
- scrape(url)

### 2. File
- read_file(path)
- write_file(path, data)

### 3. Database
- query_db(sql)
- insert_db(data)

### 4. External API
- call_api(endpoint, payload)

### 5. Communication
- send_message(channel, content)

---

## インターフェース

tool_call = {
  "tool": "",
  "input": {},
  "timeout": int,
  "retry": int
}

---

## 実行ルール

- 失敗した場合 retry
- 上限超えたら fallback