# 章節與中繼資料編輯計畫

## Overview
在 GUI 介面加入章節名稱、封面及 ID3 標籤編輯功能，輸出更完整的有聲書檔案。

## Current Problem Analysis
目前僅能選擇章節轉換，無法自訂章節標題或編輯封面，中繼資料也缺乏管理。

## Strategy and Approach
- 使用 `mutagen` 等套件處理 ID3 標籤。
- GUI 加入對話框與表單，允許使用者輸入或修改中繼資料。

## Implementation Steps
1. 研究 `mutagen` API 並實作 ID3 標籤寫入 ⏳
2. 在 `gui.py` 新增章節與封面編輯介面 ⏳
3. 更新 CLI，讓批次處理亦可指定資料 ⏳
4. 撰寫範例與文件 ✅

## Timeline
| 階段 | 預計完成 |
|------|----------|
| 基本標籤寫入 | 2024 Q4 |
| GUI 介面完善 | 2025 Q1 |

## Risk Assessment
- 跨平台 MP3/MP4 標籤處理差異。
- 使用者輸入錯誤可能造成檔案損壞。

## Success Criteria
- 使用者能在 GUI 與 CLI 自訂章節及封面，輸出檔案成功載入標籤。

## Progress Tracking
- ID3 標籤 ⏳
- GUI 介面 ⏳
- CLI 支援 ⏳
- 文件 ✅

## Related Files
- `audiblez/gui.py`
- `audiblez/cli.py`
- `audiblez/tagger.py`
