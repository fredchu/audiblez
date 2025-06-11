# 雲端或伺服器模式計畫

## Overview
提供遠端轉檔服務，讓使用者無需本地安裝即可上傳文件並下載生成的有聲書，亦可用於商業化。

## Current Problem Analysis
目前所有轉換都在使用者端進行，缺乏集中資源的方式，也阻礙可能的收費服務。

## Strategy and Approach
- 以 `FastAPI` 或 `Flask` 建立 REST API，上傳檔案後以 GPU 生成音檔。
- 透過 Docker 容器化並撰寫部署腳本，可在雲端平台快速啟動。

## Implementation Steps
1. 建立基本 API：上傳、查詢進度、下載結果 ⏳
2. 加入使用者驗證與流量控管 ⏳
3. 撰寫 Dockerfile 與部署教學 ⏳
4. 規劃收費機制或贊助方式 ✅

## Timeline
| 階段 | 預計完成 |
|------|----------|
| API 原型 | 2025 Q1 |
| 雲端部署 | 2025 Q2 |

## Risk Assessment
- 雲端資源成本高，需評估是否有回收機會。
- 安全性與權限管理必須謹慎。

## Success Criteria
- 使用者可以透過 Web API 上傳檔案並成功取得有聲書。

## Progress Tracking
- API 功能 ⏳
- 驗證與控管 ⏳
- Docker 部署 ⏳
- 收費方案 ✅

## Related Files
- `server/api.py`
- `Dockerfile`
- `docs/deploy.md`
