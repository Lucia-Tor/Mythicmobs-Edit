<div align="center">

# ⚒ MythicForge 神話工坊

**MythicMobs 5.x / MythicCrucible 視覺化編輯器**

單一 HTML 檔案 · 免安裝 · 免網路 · 用瀏覽器直接讀寫伺服器設定檔

![平台](https://img.shields.io/badge/平台-Chrome%20%2F%20Edge-4285F4?logo=googlechrome&logoColor=white)
![相依](https://img.shields.io/badge/相依-無・單檔離線可用-2ea44f)
![支援](https://img.shields.io/badge/支援-MythicMobs%205.x%20%2F%20MythicCrucible-e8a33d)
![Discord](https://img.shields.io/badge/Discord-lucia.__.03-5865F2?logo=discord&logoColor=white)

<br>

*「寫技能不用再翻英文 Wiki。」*

</div>

---

## 📖 這是什麼？

MythicForge 是一個給 Minecraft 伺服器管理員用的 **MythicMobs 設定檔編輯器**。
整個工具就是一個 `MythicForge.html`，用 Chrome 或 Edge 打開、選取伺服器的 `plugins/MythicMobs` 資料夾，就能用圖形介面編輯：

| 分類 | 說明 |
|:---:|------|
| 👹 **怪物（Mobs）** | 生物類型、屬性、AI、選項、技能列表 |
| ⚔ **物品（Items / Crucible）** | 材質、屬性、附魔、Crucible 專屬設定 |
| ✨ **技能（Skills）** | Metaskill 的機制、目標選擇器、條件、觸發器 |
| 🎁 **掉落表（DropTables）** | 掉落物與機率設定 |

<br>

## ✨ 特色

- 📦 **單檔免安裝** — 所有程式碼與資料庫都內嵌在一個 HTML 裡，不需要 Node.js、不需要連網、不會傳送任何資料到外部。
- 💾 **直接讀寫伺服器檔案** — 透過瀏覽器的 File System Access API 直接開啟 `plugins/MythicMobs`，改完存檔、遊戲內 `/mm reload` 即生效，不用複製貼上。
- 🇹🇼 **全中文技能資料庫** — 內建中文化的技能機制（Mechanics）、目標選擇器（Targeters）、條件（Conditions）、觸發器（Triggers）與怪物選項說明。
- 🔀 **表單 / YAML 雙模式** — 可以用表單點選編輯，也可以隨時切到「YAML 原始碼」直接手寫。
- 🧩 **區塊拼接存檔** — 儲存時只改寫你動過的條目區塊，檔案裡**其他條目與註解原樣保留**，不會被重新排版。
- 🗂 **檔案管理** — 側邊欄搜尋條目、新增 YAML 檔案、重新命名與刪除條目，並會記住上次開啟的資料夾。

<br>

## 🚀 快速開始

> 只要四十秒，從下載到開始編輯。

1. 下載 [`MythicForge.html`](./MythicForge.html)（點進去後按右上角 **Download raw file**）。
2. 用 **Chrome** 或 **Edge** 開啟這個檔案（雙擊即可）。
3. 點右上角「**📂 開啟 MythicMobs 資料夾**」，選擇伺服器的 `plugins/MythicMobs`。
   - 選到 `plugins` 或伺服器根目錄也沒關係，工具會自動往下找到 MythicMobs。
   - 瀏覽器會詢問資料夾存取權限，請選「允許」。
4. 左側選擇分類與條目開始編輯，<kbd>Ctrl</kbd>+<kbd>S</kbd> 儲存目前檔案。
5. 到遊戲內或後台執行 `/mm reload`，變更立即生效。

<br>

## 📋 環境需求

| 項目 | 需求 |
|------|------|
| 🌐 瀏覽器 | Chrome 或 Edge（需要 File System Access API；Firefox / Safari 不支援資料夾讀寫） |
| 🖥 伺服器端 | MythicMobs 5.x；物品編輯需另裝 MythicCrucible |
| 📁 檔案存取 | 需能直接存取伺服器檔案 —— 適合本機開服或有掛載遠端資料夾的環境 |

<br>

## ⚠️ 注意事項

> [!WARNING]
> - 儲存時只會改寫**你編輯過的條目**，檔案中其他內容原樣保留；但被編輯條目**內部**的註解會遺失。
> - 重要修改前建議先備份 `plugins/MythicMobs` 資料夾。

> [!NOTE]
> 工具完全在本機瀏覽器內執行，不會上傳或回傳任何檔案內容。

<br>

## ❓ 常見問題

<details>
<summary><b>打開後點「開啟資料夾」沒反應 / 顯示不支援？</b></summary>
<br>

請確認使用 Chrome 或 Edge，其他瀏覽器沒有實作資料夾讀寫 API。

</details>

<details>
<summary><b>可以編輯遠端主機（VPS / 託管商）的伺服器嗎？</b></summary>
<br>

工具需要直接存取檔案系統。若是遠端主機，可先把 <code>plugins/MythicMobs</code> 下載到本機編輯後再上傳，或使用 SFTP 掛載成本機磁碟。

</details>

<details>
<summary><b>存檔後遊戲內沒變化？</b></summary>
<br>

記得執行 <code>/mm reload</code>。若仍無效，檢查後台是否有 YAML 解析錯誤訊息。

</details>

<br>

---

<div align="center">

## 👤 作者與致謝

**作者**：lucia.\_.03（Discord）
有問題或建議歡迎在 Discord 上找我，或直接開 [Issue](../../issues)。

**共同開發**：本工具由 lucia.\_.03 與 **Claude**（Anthropic 的 AI 助理，透過 Claude Code）
一起討論需求、設計介面並撰寫程式碼完成。

<br>

⭐ 覺得好用的話，歡迎給個 Star！

</div>
