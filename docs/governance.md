# 文檔治理規範（Docs Governance）

> 狀態：Active
> 版本：1.0.0
> 更新日期：2026-03-25
> 適用範圍：docs/ 及其子目錄

---

## 1. 目標

建立固定的文檔增刪、歸檔與同步標準，降低資訊斷片，讓人與 AI Agent 都能穩定檢索到正確知識。

---

## 2. 文件分類與責任

### 2.1 Active 核心文件（固定入口）

- docs/todo.md：唯一 active 清單
- docs/completed.md：已完成里程碑與落地決策
- docs/roadmap.md：里程碑與產品路線
- docs/README.md：導航入口

規則：任何新工作項、狀態變更、路線調整，至少同步以上 2 份文件。

### 2.2 契約規格（docs/specs）

- 用途：定義可執行契約（schema、輸出欄位、行為邊界）
- 命名：{domain}-v{major}.md 或 {domain}-v{major}.{minor}.md
- 升版：Major（破壞性變更）、Minor（相容擴充）、Patch（文件修正）

### 2.3 決策（docs/decisions）

- 用途：記錄「為何這樣做」
- 命名：{topic}-decision-YYYY-MM-DD.md
- 規則：決策核准當日新增，並在 completed 補摘要

### 2.4 歸檔（docs/archive）

- 用途：保留歷史，不作現行執行依據

### 2.5 臨時性文件（docs/drafts）

- 用途：會議記錄、草稿、實驗性構想
- 規則：
  - 不受同步責任約束
  - 確定落地後需移至對應分類（specs/decisions）
  - 超過 30 天未轉正，自動歸檔或刪除

---

## 3. 異動檢查點

- **新增**：更新 README 導航 + 留引用（todo/completed）
- **修改**：更新日期 + 依 §5 同步矩陣執行
- **刪除**：歸檔至 archive/{yyyy-mm}-* + 留替代說明 + 記錄於 completed

---

## 4. 歸檔觸發條件

符合任一條件可歸檔：
- 已被新版規格完全取代
- 僅供歷史追溯，非當前執行依據
- 連續一個里程碑以上未被引用（在 todo/roadmap/completed 中無連結或關鍵字）

歸檔後必須：
- 不再出現在 active 優先閱讀路徑
- 在 README 或主規格提供 archive 入口

---

## 5. 同步責任矩陣（影響範圍驅動）

按實際影響範圍決定同步標的，非一律同步多份文件：

| 異動類型 | 影響範圍 | 必須同步 | 選填同步 |
|---------|---------|---------|----------|
| 需求/優先級變動 | 里程碑排程 | todo + roadmap | - |
| 階段性任務完成 | 單一任務 | completed（移出 todo） | roadmap（若影響里程碑） |
| 契約規格升版 | API 行為變更 | specs + completed | README（若為核心契約） |
| 重大決策落地 | 架構方向 | decisions + completed | roadmap（若影響路線圖） |
| 純文件潤飾 | 不影響執行 | 僅該文件本身 | - |

檢查點：
- 修改前問：「這會影響其他文件的使用者嗎？」
- 若答案為「否」，僅更新該文件即可

---

## 6. AI Agent 查找順序（強制）

1. docs/README.md
2. docs/todo.md
3. docs/completed.md
4. docs/roadmap.md
5. docs/specs/*（依目標領域）
6. docs/decisions/*
7. docs/archive/*（僅追溯）

---

## 7. 驗證機制

**異動檢查：** 更新日期 + 依 §5 確認同步 + 契約升版需遞增版本號 + 歸檔需留替代說明

**違規處理：** 發現時於下次編輯一併修正，非阻塞性違規可延後，僅向前適用

---

## 8. 本專案當前治理重點（2026-03）

- semantic graph 契約已升至 v1.1（完整性訊號上線）
- 優先確保 active-only，不讓已完成內容回流至 todo
- Web 模式文件規劃需在 integrityStatus 穩定後啟動
