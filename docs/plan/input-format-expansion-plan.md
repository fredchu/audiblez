# 支援更多輸入格式計畫

## Overview
擴充 Audiblez 能讀取的檔案類型，除了現有的 EPUB，還包括 Markdown、純文字及 PDF，以吸引更多使用者。

## Current Problem Analysis
目前 GUI 中雖然有標示這些選項，但處理流程尚未實作，導致使用者只能轉換 EPUB。

## Strategy and Approach
- 啟用 GUI 與 CLI 的檔案篩選與讀取流程。
- 依檔案類型使用 `pandoc` 或其他套件轉成文字，再進入現有 TTS 流程。

## Implementation Steps
1. 修改 `audiblez/gui.py` 的開啟檔案對話框，加入 .md、.txt、.pdf 篩選 ⏳
2. 在 `audiblez/cli.py` 中解析新格式的參數 ⏳
3. 新增轉檔模組 `audiblez/converter.py` 處理多格式輸入 ⏳
4. 撰寫單元測試與文件 ✅

## Timeline
| 階段 | 預計完成 |
|------|----------|
| 基本讀取與轉換 | 2024 Q3 |
| 完成測試與文件 | 2024 Q4 |

## Risk Assessment
- `pandoc` 或其他套件授權問題。
- PDF 解析可能產生排版錯誤。

## Success Criteria
- 使用者可順利載入並轉換 Markdown、純文字及 PDF。

## Progress Tracking
- 檔案對話框更新 ⏳
- CLI 解析 ⏳
- 轉檔模組實作 ⏳
- 測試與文件 ✅

## Related Files
- `audiblez/gui.py`
- `audiblez/cli.py`
- `audiblez/converter.py`
