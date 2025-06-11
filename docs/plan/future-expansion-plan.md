# Future Expansion Plan

## Overview
This document outlines potential expansion and development directions for the audiblez project. These ideas are based on the current roadmap in `TODO_zh-TW.md` and community suggestions.

## Current Problem Analysis
- Only EPUB files are supported; other document formats remain commented out in the GUI.
- Voice options are limited to the predefined Kokoro voices.
- Distribution is currently source-based, which is inconvenient for non-technical users.
- There is no cloud service option to offload processing from user machines.
- Metadata editing in the GUI is minimal, and integration with other tools is lacking.

## Strategy and Approach
- Gradually enable additional input formats and support more TTS engines.
- Provide cross-platform packaging for easier installation.
- Offer optional cloud-based conversion services for convenience and potential commercialization.
- Expand GUI features for metadata editing and integration with ebook managers.
- Encourage contributions and sponsorships to sustain development.

## Implementation Steps
1. **Enable Additional Formats** ⏳
   - Activate support for Markdown, plain text, and PDF in `audiblez/ui.py`.
   - Implement conversion pipelines using tools like `pandoc`.
2. **Add Voice and TTS Options** ⏳
   - Evaluate other TTS engines (e.g., Coqui TTS).
   - Update `audiblez/voices.py` and expose settings in CLI/GUI.
3. **Cross-Platform Packaging** ⏳
   - Use `PyInstaller` or `cx_Freeze` to create installers for Windows, macOS, and Linux.
   - Add automation scripts for builds.
4. **Cloud or Server Mode** ⏳
   - Create a REST API using FastAPI or Flask.
   - Provide Docker deployment guides.
5. **Metadata Editing and Tool Integration** ⏳
   - Extend the GUI for chapter renaming and cover art management.
   - Investigate Calibre integration for importing and syncing books.
6. **Commercialization and Sponsorship** ⏳
   - Add donation links to the README.
   - Evaluate freemium options for premium voice packs or hosted services.

## Timeline
| Feature | Target Date |
| ------- | ----------- |
| Additional Formats | Q3 2024 |
| Voice Options | Q3 2024 |
| Cross-Platform Packaging | Q4 2024 |
| Cloud Service | Q1 2025 |
| Metadata & Integration | Q1 2025 |
| Sponsorship & Monetization | Q2 2025 |

## Risk Assessment
- **Licensing**: Ensure compliance when using external TTS models or distributing binaries.
- **Resource Usage**: Cloud services may incur costs for GPU usage.
- **Maintenance**: Supporting multiple platforms and engines increases complexity.

## Success Criteria
- Users can load Markdown, text, and PDF files without errors.
- Multiple voice engines are selectable in the GUI and CLI.
- Standalone installers are downloadable for major OSes.
- A simple web API is available for remote conversion.
- GUI supports metadata editing and integrates with Calibre.
- Project receives donations or sponsors to fund ongoing work.

## Progress Tracking
- Additional Formats: ⏳
- Voice and TTS Options: ⏳
- Cross-Platform Packaging: ⏳
- Cloud or Server Mode: ⏳
- Metadata Editing and Tool Integration: ⏳
- Commercialization and Sponsorship: ⏳

## Related Files
- `audiblez/ui.py`
- `audiblez/cli.py`
- `audiblez/voices.py`
- `README.md`
- `TODO_zh-TW.md`
