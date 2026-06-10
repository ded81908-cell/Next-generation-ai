# Config System

## 目的
ハードコード防止・柔軟制御

---

## 設定例

config = {
  "max_retry": 3,
  "timeout": 10,
  "max_agents": 10,
  "model_default": "mini",
  "model_advanced": "claude",
  "cost_limit": 100
}

---

## 読み込み

load_config()
update_config()

---

## 動的変更

if performance_drop:
    adjust_threshold()