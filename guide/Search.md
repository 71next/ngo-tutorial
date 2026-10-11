以下是一份可直接複製、貼進筆記或 Notion 的 **GitHub Search Keywords Markdown**。搜尋語法為 `關鍵字 qualifier:value`；多個條件以空格分隔，預設為 AND；精確字串用雙引號、regex 用斜線。 [docs.github](https://docs.github.com/en/search-github/github-code-search/understanding-github-code-search-syntax)

# GitHub Search Keywords

## 基本規則

```text
關鍵字 language:程式語言 stars:>最低星數 pushed:>YYYY-MM-DD
```

- 多個條件用空格分隔，預設是 `AND`
- 含空格的精確字串：`"LINE Messaging API"`
- 排除條件：`-language:javascript` 或 `NOT archived:true`
- regex：`/\d{4}-\d{2}-\d{2}/`
- Code Search 必須切到 **Code** 分頁；Repository 搜尋則切到 **Repositories** 分頁。 [docs.github](https://docs.github.com/en/search-github/github-code-search/understanding-github-code-search-syntax)

## 常用 Qualifier

| Qualifier | 用途 | 範例 |
|---|---|---|
| `stars:` | Star 數 | `stars:>1000` |
| `forks:` | Fork 數 | `forks:>100` |
| `language:` | 程式語言 | `language:python` |
| `topic:` | GitHub Topic | `topic:wordpress` |
| `user:` | 特定使用者 | `user:vinta` |
| `org:` | 特定組織 | `org:vercel` |
| `repo:` | 特定 repository | `repo:vercel/next.js` |
| `pushed:` | 最後 push 時間 | `pushed:>2026-01-01` |
| `created:` | 建立時間 | `created:>2025-01-01` |
| `license:` | 授權條款 | `license:mit` |
| `archived:` | 是否封存 | `archived:false` |
| `fork:` | 是否包含 fork | `fork:false` |
| `in:` | 搜尋範圍 | `in:name,description` |
| `path:` | 檔案路徑 | `path:src` |
| `filename:` | 檔名 | `filename:.env` |
| `symbol:` | 函式／類別定義 | `symbol:createOrder` |

`repo:` 必須寫完整名稱，例如 `repo:vercel/next.js`；`path:` 用來限定路徑，`symbol:` 只搜尋符號定義，不搜尋引用位置。 [docs.github](https://docs.github.com/en/search-github/github-code-search/understanding-github-code-search-syntax)

# 找專案 Repositories

## 熱門開源專案

```text
machine learning language:python stars:>5000
```

```text
llm agent framework language:typescript stars:>1000
```

```text
rag knowledge base language:python stars:>500 pushed:>2026-01-01
```

```text
vector database language:python stars:>1000 pushed:>2026-01-01
```

```text
automation workflow language:typescript stars:>500 pushed:>2026-01-01
```

## WordPress

```text
wordpress plugin language:php stars:>100 pushed:>2026-01-01
```

```text
wordpress theme language:php stars:>300 pushed:>2026-01-01
```

```text
wordpress ai in:description language:php stars:>20
```

```text
wordpress 會員 in:readme language:php stars:>30
```

```text
wordpress 教學 in:readme stars:>50
```

## AI / RAG / Agent

```text
rag 知識庫 in:readme language:python stars:>100
```

```text
llm 中文 in:readme stars:>500
```

```text
ai agent framework language:python stars:>1000
```

```text
mcp server language:typescript stars:>100 pushed:>2026-01-01
```

```text
prompt engineering stars:>1000 pushed:>2026-01-01
```

## n8n / 自動化

```text
n8n workflow stars:>50 pushed:>2026-01-01
```

```text
n8n 中文 in:readme stars:>20
```

```text
n8n template stars:>30
```

```text
workflow automation language:typescript stars:>500
```

## LINE / 企業整合

```text
line bot language:python stars:>100 pushed:>2026-01-01
```

```text
"LINE Messaging API" language:php stars:>20
```

```text
line login language:typescript stars:>50
```

```text
line bot 教學 in:readme language:python stars:>50
```

## UI / UX / Figma

```text
figma plugin language:typescript stars:>100
```

```text
figma design system language:typescript stars:>200
```

```text
ui components language:typescript stars:>1000
```

```text
vue component library language:typescript stars:>1000
```

# 找中文資源

## 中文教學與文件

```text
AI 教學 in:readme stars:>100
```

```text
wordpress 教學 in:readme stars:>50
```

```text
n8n 中文 in:readme stars:>30
```

```text
RAG 知識庫 in:readme language:python stars:>100
```

```text
LLM 中文 in:readme stars:>500
```

## 台灣相關專案

```text
台灣 in:description stars:>100
```

```text
Taiwan language:python stars:>100
```

```text
台灣 開源 in:readme stars:>50
```

## 繁簡體轉換查詢

GitHub 不一定會自動做繁簡轉換，重要詞建議分開查詢：

```text
會員登入
```

```text
会员登录
```

```text
"會員登入" OR "会员登录"
```

```text
"訂單編號" OR "订单编号"
```

# 找特定作者或組織

```text
user:vinta awesome
```

```text
org:vercel next.js
```

```text
org:openai language:python stars:>100
```

```text
repo:vercel/next.js router
```

```text
user:你的GitHub帳號 language:php
```

```text
org:你的組織 "LINE Messaging API"
```

# 找程式碼 Code Search

切換到 GitHub 的 **Code** 分頁後使用。

## 單一 Repo

```text
repo:vercel/next.js "createServer"
```

```text
repo:你的帳號/你的repo "訂單編號"
```

```text
repo:你的帳號/你的repo "createOrder" language:typescript
```

## 組織內搜尋

```text
org:你的組織 "axios.post" language:typescript
```

```text
org:你的組織 "LINE Messaging API" language:php
```

```text
org:你的組織 "webhook" language:typescript
```

## 檔案與路徑

```text
repo:你的帳號/你的repo "login" path:src
```

```text
repo:你的帳號/你的repo "API_KEY" filename:.env
```

```text
repo:你的帳號/你的repo "function" language:php
```

```text
repo:你的帳號/你的repo "useState" language:typescript
```

## Regex

```text
repo:你的帳號/你的repo /\d{4}-\d{2}-\d{2}/
```

```text
repo:你的帳號/你的repo /https?:\/\/[^\s]+/
```

```text
repo:你的帳號/你的repo /function\s+\w+\(/ language:javascript
```

GitHub Code Search 支援以斜線包住的 regex，例如 `/\d{4}-\d{2}-\d{2}/`；`path:` 限定路徑，`filename:` 限定檔名。 [docs.github](https://docs.github.com/en/search-github/github-code-search/understanding-github-code-search-syntax)

# 找 Issue 與 PR

## Issue

```text
is:issue is:open label:bug
```

```text
is:issue is:open 中文
```

```text
is:issue author:octocat
```

```text
is:issue is:open label:"good first issue"
```

## Pull Request

```text
repo:vercel/next.js is:pr is:open
```

```text
org:vercel is:pr is:open label:bug
```

```text
is:pr is:open author:你的GitHub帳號
```

## 排除條件

```text
is:issue -is:closed
```

```text
is:pr -is:draft
```

```text
is:issue is:open -label:wontfix
```

# 高品質專案搜尋模板

## 通用模板

```text
主題 language:語言 stars:>300 pushed:>YYYY-MM-DD -archived:true
```

範例：

```text
wordpress ai language:php stars:>50 pushed:>2026-01-01 -archived:true
```

```text
rag knowledge base language:python stars:>300 pushed:>2026-01-01 -archived:true
```

```text
line bot language:python stars:>100 pushed:>2026-01-01 -archived:true
```

## 找最近活躍專案

```text
主題 pushed:>2026-06-01 stars:>100
```

範例：

```text
n8n workflow pushed:>2026-06-01 stars:>50
```

## 找適合學習的專案

```text
主題 topic:sample stars:>100
```

```text
主題 example language:typescript stars:>200
```

```text
主題 tutorial language:python stars:>100
```

# 快速複製區

## WordPress

```text
wordpress plugin language:php stars:>100 pushed:>2026-01-01 -archived:true
```

```text
wordpress ai in:description language:php stars:>20
```

```text
wordpress 會員 in:readme language:php stars:>30
```

## AI / RAG

```text
rag knowledge base language:python stars:>500 pushed:>2026-01-01
```

```text
llm agent framework language:typescript stars:>1000
```

```text
mcp server language:typescript stars:>100 pushed:>2026-01-01
```

## n8n / LINE

```text
n8n workflow stars:>50 pushed:>2026-01-01
```

```text
n8n 中文 in:readme stars:>20
```

```text
line bot language:python stars:>100 pushed:>2026-01-01
```

```text
"LINE Messaging API" language:php stars:>20
```

## Figma / Vue

```text
figma plugin language:typescript stars:>100
```

```text
vue component library language:typescript stars:>1000
```

```text
ui components language:typescript stars:>1000
```

## 常用排除寫法

```text
-archived:true
```

```text
fork:false
```

```text
-language:javascript
```

```text
-topic:sample
```

```text
-license:gpl-3.0
```

# 搜尋建議

- 找專案時，優先用 `stars:` + `pushed:` + `-archived:true`，可過濾停更與封存 repo。 [apify](https://apify.com/ryanclinton/github-repo-search)
- 找中文內容時，加上 `in:readme`、`in:description` 或 `in:name`，並同時測試繁體與簡體關鍵字。
- 找程式碼時，先用 `repo:`、`org:` 或 `user:` 限定範圍，避免全 GitHub 搜尋造成大量雜訊。 [docs.github](https://docs.github.com/en/search-github/github-code-search/understanding-github-code-search-syntax)
- `symbol:` 適合找函式或類別的定義；若要找所有呼叫位置，建議改用精確字串或 regex，並搭配 `repo:` / `org:` 限定。 [github](https://github.com/github/docs/blob/main/content/search-github/github-code-search/about-github-code-search.md)