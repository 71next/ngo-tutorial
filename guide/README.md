# 講師教案｜公民組織的 GitHub 資源搜索與選擇指南

搭配簡報：[`slides/index.html`](../slides/index.html)（19 頁，按 N 看講者備註）

## 課程資訊與學習目標

90 分鐘線上交流會，對象為非技術背景的公民組織成員；全程只用瀏覽器操作 GitHub 網頁，不安裝 Git、不寫程式。

| 項目 | 內容 |
| --- | --- |
| 形式 | 線上（視訊會議＋螢幕分享），講述 40%、實作 60% |
| 人數建議 | 15–30 人；超過 20 人建議安排 1 位助教看聊天室 |
| 先備條件 | 會用瀏覽器、已註冊 GitHub 帳號 |
| 搭配教材 | 上課簡報（19 頁，含講者備註）、學員講義（10 頁 A4） |

課程結束後，學員能夠：

1. 用自己的話說明 Repository、README、Star、Fork、Release、License 的意思
2. 在 GitHub 用關鍵字加篩選條件（topic、stars、pushed、license、org）找到符合需求的專案
3. 用六項健康檢查判斷一個專案適不適合組織採用
4. 用 Releases、Download ZIP、Fork 取得資源，並在網頁上建立 Repo、上傳檔案
5. 用 AI 工具找候選專案、讀懂專案，並自行查證網址與授權

## 課前準備清單

講師端（課前 1–3 天）：

- [ ] 寄出行前通知：請學員先到 github.com/signup 註冊並驗證 Email
- [ ] 準備示範專案 2–3 個（建議 g0v 組織內一個、有 Releases 的一個、無 License 的一個當反例）
- [ ] 確認 GitHub Copilot 免費方案目前的對話額度（github.com/features/copilot/plans），額度規則今年有調整過
- [ ] 準備一個 AI 聊天工具的示範帳號，先試跑一次提示詞範本
- [ ] 準備上傳練習素材：一份 .md 活動說明或一張海報圖片，放在雲端讓學員下載
- [ ] 簡報封面填入講師姓名、日期、主辦單位

上課當天（開場前 10 分鐘）：

- [ ] 瀏覽器開好分頁：github.com、github.com/topics/civic-tech、github.com/g0v、deepwiki.com
- [ ] 示範用瀏覽器字體放大到 125% 以上，方便線上觀看
- [ ] 聊天室置頂今日練習網址與提示詞範本

## 90 分鐘時間分配

實作集中在後半段（50–85 分），前 50 分鐘以示範為主，讓學員先建立地圖再動手。

| 時間 | 單元 | 分鐘 | 形式 | 對應簡報 |
| --- | --- | --- | --- | --- |
| 00–05 | 開場：課程目標與流程 | 5 | 講述 | 1–3 |
| 05–20 | 一、GitHub 觀念與基本術語 | 15 | 講述＋比喻 | 4–5 |
| 20–35 | 二、導覽 GitHub 平台介面 | 15 | 螢幕示範 | 6 |
| 35–50 | 三、導覽 Repository 頁面與健康檢查 | 15 | 示範＋檢查表 | 7–9 |
| 50–75 | 四、搜尋、下載、上傳練習 | 25 | 實作 | 10–13 |
| 75–85 | 五、如何找資源：語法、清單與 AI | 10 | 示範＋實作 | 14–18 |
| 85–90 | 歸納重點與 Q&A | 5 | 交流 | 19 |

時間不夠時的刪減順序：先縮短第二單元的 Explore／Trending 示範，再把上傳練習改為講師示範。

## 各單元講稿重點與操作步驟

### 開場（00–05）

- 自我介紹，說明今天只用瀏覽器、不寫程式
- 拋問題暖場：「你的組織最近想做但沒預算做的工具是什麼？」請學員打在聊天室，後面練習會用到
- 確認大家已登入 GitHub；還沒註冊的人邊聽邊註冊

### 一、觀念與基本術語（05–20）

- 核心一句話：Git 是記錄修改的工具，GitHub 是放這些專案的線上圖書館
- 十個術語逐一講，但強調今天最常用五個：Repository、README、Star、Release、License
- 圖書館比喻延伸：Fork＝影印一本書回家加註；Issue＝意見箱；Pull Request＝寫信請作者收錄你的修正
- 互動：請學員在聊天室用一句話解釋「Fork」，確認理解

### 二、平台介面導覽（20–35）

螢幕示範，依序操作：

1. 登入後的首頁（Dashboard）
2. 右上角頭像選單：Your profile、Your repositories、Your stars
3. 頂部搜尋列，示範按「/」快捷鍵
4. github.com/explore 與 github.com/trending
5. github.com/topics/civic-tech、github.com/topics/open-data
6. 組織頁 github.com/g0v，說明台灣公民科技社群

補充（簡報第 6 頁兩個彈窗）：

- **Explore 各分頁**：Topics（依主題標籤列出同類專案，找工具最有用）、Trending（星數漲最快，多半是 AI 與開發工具）、Collections（GitHub 人工整理的專題清單）、Events（活動，本課用不到）、Sponsors（贊助開源開發者）
- **Marketplace 是 GitHub 的外掛商店**：Apps（接到 Repo 的第三方服務，如 Codecov、Crowdin）與 Actions（自動測試、自動部署）。學員常誤以為是「開源軟體商店」，要說明找志工、捐款等工具要到 Repositories 用搜尋語法與 Topics 找

提醒：GitHub 沒有官方中文介面，可用瀏覽器右鍵「翻譯成中文」。

### 三、Repository 頁面與健康檢查（35–50）

- 打開一個實際專案，依簡報第 7 頁截圖上的編號①–⑦逐一指出位置（截圖可往下捲動到 README）
- 重點講三處：README（做什麼）、License（能不能用）、最後 Commit 時間（有沒有人維護）
- 帶過六項健康檢查表（簡報第 8 頁），用一個好專案和一個沒有 License 的專案對照
- 授權觀念（簡報第 9 頁）：MIT、Apache 是寬鬆授權，可用、可改、可商用，保留原作者聲明即可；GPL、AGPL 是互惠授權，把修改版發給別人（AGPL 連放上網站給人用也算）時要用相同授權公開原始碼；文件與資料常見 CC 授權（BY 標示出處、NC 不可商用、ND 不可改作、SA 相同方式分享）；沒有 License 的專案預設保留所有權利，看得到不等於可以用

### 四、搜尋、下載、上傳練習（50–75）

**搜尋語法講解（5 分鐘）**：示範簡報第 10 頁語法，最後示範組合範例。補充：搜尋結果頁左側可切換 Repositories／Code／Issues，右上可依 Most stars、Recently updated 排序。

**搜尋練習（10 分鐘）**：

1. 在 g0v 組織裡找一個開放資料相關專案（提示：`org:g0v open data`）
2. 找一個近一年有更新、MIT 授權的志工或活動報名工具（提示：`volunteer license:mit pushed:>2025-10-01`）
3. 用健康檢查表打分數並按 Star 收藏，把網址貼到聊天室

**下載練習（3 分鐘）**：對收藏的專案試 Download ZIP，再找一個有 Releases 的專案看 Assets。提醒只從可信任的專案下載執行檔。可點簡報第 12 頁的「Tag 跟 Release 有什麼不同？」彈窗補充：Tag 只是幫某次 Commit 貼上版本號的書籤；Release 是建在 Tag 上的說明頁，可附安裝檔，所以要下載軟體看 Releases 就好。

**上傳練習（7 分鐘）**：

1. 右上角「＋」→ New repository
2. 命名（例：`my-first-repo`）、選 Private 練習較安心、勾選 Add a README file → Create repository
3. Add file → Upload files，拖曳練習素材
4. 在 Commit 訊息寫一句說明 → Commit changes
5. 點 Commits 看剛才的紀錄，呼應「Commit＝一次存檔」

### 五、如何找資源：語法、清單與 AI（75–85）

- 先說明站內搜尋為什麼常找不到：它只比對名稱、說明、README 的文字，不會理解需求，中文描述多半搜不到（簡報第 14 頁）
- 四種手法：下對搜尋語法、逛 Topics 與「awesome＋主題」清單、順著好專案的作者與組織找、請 AI 提名；可以混用
- 進階語法（簡報第 15 頁）以「找軟體工具」為例，示範兩三個就好：`topic:self-hosted` 找可自己架的開源替代品、`topic:android` 找可安裝的 App、`awesome` 找整理好的清單、`-topic:library` 排除給工程師用的程式庫；找到後看右側 Releases 或 README 的 Demo／線上版；提醒結果頁左側要切到對的類型（Repositories、Issues）
- 三種工具分工：通用 AI 聊天（找之前，幫忙想關鍵字與候選）、DeepWiki（看懂時，把網址的 github.com 換成 deepwiki.com）、GitHub Copilot Chat（站內問，免費方案有每月額度）
- 現場示範提示詞範本（簡報第 17 頁），把 AI 推薦的網址逐一點開，示範有時會找不到或內容不符
- 學員實作 5 分鐘：把範本中括號換成自己組織的需求
- 收尾觀念：AI 負責提名，你負責查證；不要把會員名單等個資貼進 AI

### 歸納重點與 Q&A（85–90）

- 唸過簡報第 19 頁五項重點
- 請學員在聊天室留下今天收藏的一個專案與用途，整理成課後交流清單

## 常見問題與卡關排解

| 狀況 | 處理方式 |
| --- | --- |
| 註冊時收不到驗證信 | 檢查垃圾郵件匣；改用 Gmail 重新註冊 |
| 搜尋結果看起來是程式碼不是專案 | 結果頁左側切到 Repositories |
| 日期篩選沒作用 | 日期要寫成 YYYY-MM-DD，例 `pushed:>2025-10-01` |
| 中文關鍵字搜不到 | 改用英文，或請 AI 幫忙翻成英文關鍵字 |
| 找不到 Download ZIP | 要在 Code 分頁，點綠色「Code」按鈕才會出現 |
| 專案沒有 Releases | 改用 Download ZIP，或看 README 是否有線上版網址 |
| 上傳後找不到檔案 | 確認有按 Commit changes；重新整理頁面 |
| AI 給的網址打不開 | 可能是 AI 編造或專案已刪除，回 GitHub 用名稱搜尋確認 |
| 學員問「這可以商用嗎」 | 看 License 檔原文；組織正式採用前請懂授權的夥伴確認 |

## 課後資源與參考來源

- [GitHub 官方文件：搜尋 Repository 的語法](https://docs.github.com/en/search-github/searching-on-github/searching-for-repositories)
- [GitHub 主題：civic-tech](https://github.com/topics/civic-tech)
- [g0v 零時政府 GitHub 組織頁](https://github.com/g0v)
- [DeepWiki 介紹（Cognition）](https://cognition.ai/blog/deepwiki)：公開專案免費，把網址的 github.com 換成 deepwiki.com
- [GitHub Copilot 個人設定說明](https://docs.github.com/en/copilot/how-tos/copilot-on-github/set-up-copilot/enable-copilot/set-up-for-self)：免費方案提供有限的對話與補全額度
