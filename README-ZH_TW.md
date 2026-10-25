[简体中文](README.md) | [English](README-EN.md) | **繁體中文**

# PCL-CE unrestrict

跟隨 [PCL 社群版（PCL-CE）](https://github.com/PCL-Community/PCL-CE) 官方發行，自動建置解除地區功能限制的版本。

這是個人維護的非官方 fork。程式碼與主要功能來自上游；修改集中於 `RestrictedFeaturePolicy.cs`，保留地區評估，讓功能限制檢查直接通過。

## 下載

前往 [Releases](https://github.com/RyanWu080/PCL-CE-unrestrict/releases)，下載檔名包含 `unrestrict.exe` 的附件。Intel / AMD Windows 電腦選擇 x64，Windows ARM 裝置選擇 ARM64。需要 [.NET 10 Desktop Runtime](https://get.dot.net/10)。

GitHub 自動提供的原始碼壓縮檔對應官方原始標籤。實際套用的修補程式位於 `.github/release-sync/RestrictedFeaturePolicy.cs`；建置來源與檔案校驗值記錄於附件 `unrestrict-build.json`。

## 自動發行

- 從 **v2.15.1 正式版**開始；不補發更舊版本或 v2.15.1 的舊 Beta。後續更高版本的正式版與 Beta 都會跟隨。
- 每小時第 41 分鐘檢查官方 Release，GitHub 排程可能延遲。
- 使用官方對應標籤的原始碼，套用修補程式後建置 x64、ARM64，成功後才公開發行。
- 標籤、標題、說明與正式 / Beta 標記跟隨官方，執行檔名稱加入 `unrestrict`。已發行的執行檔不重複建置，官方說明更新時會同步。
- 限制程式碼變更、修補不相容或編譯失敗時，停止該版本的發行並等待檢查。

Release 說明沿用官方原文，其中的外部下載連結與簽章資訊屬於官方版本；本 fork 的修改版請使用本倉庫的 Assets。

## 分支與驗證範圍

`dev` 保存本 fork 的說明與自動化設定；`custom/dev-unrestricted` 每小時第 23 分鐘合併上游開發程式碼，保留獨立修補提交，衝突時停止、不強制推送，其中的說明文件沿用上游。發行建置獨立使用官方版本標籤。

工作流程為 `sync-custom-dev.yml` 與 `follow-official-releases.yml`。已驗證同步、版本篩選、編譯與發行；實際啟動、登入、下載仍需執行驗證。建置未包含官方私有服務金鑰，依賴這些金鑰的功能可能與官方不同；官方簽章不適用於修改後的執行檔。

## 來源與授權

上游為 [PCL-Community/PCL-CE](https://github.com/PCL-Community/PCL-CE)，基於龍騰貓躍的 PCL 開放原始碼，由社群開發者維護。`Plain Craft Launcher 2/` 沿用原有[自訂授權](Plain%20Craft%20Launcher%202/LICENCE)，其餘目錄沿用 [Apache License 2.0](LICENSE)。保留原有授權、著作權與作者歸屬。

本 fork 的自動化與解除限制問題請先在本倉庫排查，勿當作官方發行版回報。
