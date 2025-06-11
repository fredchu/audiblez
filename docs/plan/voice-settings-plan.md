# 新增語音與音色設定計畫

## Overview
提供更多語音引擎及音色選擇，讓使用者能依喜好調整聆聽體驗。

## Current Problem Analysis
目前僅支援預設 Kokoro 聲音，缺乏其他 TTS 引擎與細部設定，限制了可用性與彈性。

## Strategy and Approach
- 研究並整合如 Coqui TTS 等開源語音引擎。
- 在 `audiblez/voices.py` 增加多種音色，並於 CLI 與 GUI 讓用戶切換。

## Implementation Steps
1. 評估外部 TTS 引擎並處理授權事宜 ⏳
2. 調整 `voices.py` 及相關模組載入邏輯 ⏳
3. 在 GUI 及 CLI 增加音色選單與參數 ⏳
4. 撰寫範例與文件 ✅

## Timeline
| 階段 | 預計完成 |
|------|----------|
| 引擎選型與整合 | 2024 Q3 |
| GUI/CLI 選項完成 | 2024 Q4 |

## Risk Assessment
- 不同引擎可能需要額外依賴或較大的模型體積。
- 音質與語調差異需測試以避免退化。

## Success Criteria
- 使用者可在介面中自由選擇多種音色並正確輸出。

## Progress Tracking
- 引擎評估 ⏳
- `voices.py` 更新 ⏳
- GUI/CLI 選項 ⏳
- 文件 ✅

## Related Files
- `audiblez/voices.py`
- `audiblez/gui.py`
- `audiblez/cli.py`
