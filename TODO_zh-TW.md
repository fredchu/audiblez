待辦事項（未來擴展方向）
============================

以下待辦事項依據當前專案狀態拆分為可執行的小任務，提供開發上的建議與提醒。請依照實際需求調整優先順序。

### 1. 支援更多輸入格式（難度：3／5，價值：4／5）
- [ ] 啟用 UI 內已註解的 Markdown、純文字與 PDF 讀取功能。
  - 修改 `audiblez/gui.py`：將開啟檔案對話框的過濾器加入 `.md`、`.txt` 與 `.pdf`。
  - 建立相對應的轉檔處理流程，可使用 `pandoc` 或 Python 相關套件讀取後轉成文本。
  - **原因**：許多電子書或文件並非 EPUB 格式，擴充支援能吸引更多使用者並提升工具實用性。

### 2. 新增語音/音色設定選項（難度：3／5，價值：3／5）
- [ ] 在 GUI 中提供更多語音引擎與音色選擇。
  - 研究其他 TTS 引擎（例如 Coqui TTS）。
  - 於 `audiblez/voices.py` 新增或整理更多可用音色，並在 `cli.py` 及 GUI 中加入設定項目。
  - **原因**：使用者可依喜好挑選聲線與語氣，提升聆聽體驗並展現專案彈性。

### 3. 跨平台打包（難度：3／5，價值：4／5）
- [ ] 規劃使用 `PyInstaller` 或 `cx_Freeze` 打包成可執行檔。
  - 分別測試 Windows/macOS/Linux 環境相容性。
  - 撰寫 `Makefile` 或腳本自動化打包流程。
  - **原因**：降低安裝門檻，方便非技術使用者直接下載使用。

### 4. 雲端或伺服器模式（難度：5／5，價值：5／5）
- [ ] 建立 REST API 介面，供使用者上傳檔案並取得生成後的音檔。
  - 建議使用 `FastAPI` 或 `Flask`，並加上基本驗證機制。
  - 部署教學：可選用 Docker 容器化並發布到常見雲端平台。
  - **原因**：提供無需本地安裝的服務，亦可集中使用 GPU 等硬體資源，加速處理並具商業潛力。

### 5. 章節與中繼資料編輯（難度：3／5，價值：3／5）
- [ ] 擴充 GUI 讓使用者修改章節名稱、封面與其他 ID3 標籤。
  - 於 `audiblez/gui.py` 加入表單或對話框。
  - 研究 `mutagen` 套件處理 MP3/MP4 標籤。
  - **原因**：可輸出更完善的有聲書檔案，方便在播放器或管理工具中使用。

### 6. 整合其他工具（難度：4／5，價值：3／5）
- [ ] 與電子書管理軟體（如 Calibre）整合。
  - 開發 CLI / GUI 選項，直接從其資料庫匯入或同步書籍。
  - 撰寫教學文件說明整合步驟。
  - **原因**：讓現有電子書管理流程更順暢，省去重複操作，可提升專案能見度。

### 7. 商業化與贊助（難度：2／5，價值：4／5）
- [ ] 在 README 增加贊助連結（GitHub Sponsors、Patreon 等）。
- [ ] 研究「核心功能免費、進階功能收費」的方式，例如雲端快速轉檔或高品質語音包。
  - 評估授權與外部模型的使用條款，確保商業化合規。
  - **原因**：提供專案長期維護與開發動力，也有助於引入更多資源擴充功能。