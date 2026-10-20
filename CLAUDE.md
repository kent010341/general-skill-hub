# general-skill-hub

收容日常用途 skill 的 Claude Code plugin marketplace（不限於聊天、潤稿、翻譯、股市、旅遊等）。使用者以 `/plugin marketplace add kent010341/general-skill-hub` 加入。

## 撰寫 skill

- 所有 skill 一律用 Anthropic 的 `skill-creator` skill 撰寫或修改。
- 來源多半是既有 prompt（如 ChatGPT MyGPT），改寫時忠於原意：不確定就問使用者，嚴禁自行延伸規則或功能。
- 文件與 skill 內容使用繁體中文。

## 目錄結構

每個 skill 各自是一個 plugin，可單獨安裝：

```
.claude-plugin/marketplace.json              # marketplace 清單，每個 plugin 一筆
plugins/<plugin>/.claude-plugin/plugin.json  # plugin manifest（含 version）
plugins/<plugin>/skills/<skill>/SKILL.md
```

plugin 名稱與 skill 名稱相同，呼叫方式為 `/<plugin>:<skill>`。

新增 skill 時：

1. 建立上述 plugin 目錄與 `plugin.json`，初始版本 `0.1.0`。
2. 在 `marketplace.json` 的 `plugins` 新增一筆。
3. 更新 `README.md` 的 Plugins 表格。
4. 驗證：`claude plugin validate .` 與 `claude plugin validate ./plugins/<plugin>`。

## 版本

- 各 plugin 在 `plugin.json` 獨立以 semver 管理。已推送的 plugin 只要內容有變動就要升版，否則使用者收不到更新。
  - patch：措辭、錯字等不影響行為的修改
  - minor：新增或調整行為
  - major：移除功能、改名等不相容變更
- marketplace 本身不另設版本。

## Git

- 已授權 AI agent 直接 commit 並 push，不需再詢問。
- 單一 `master` 分支，直接提交，不開 develop 或 feature branch、不發 PR。
- Commit 訊息採 Conventional Commits，scope 用 plugin 名稱，例如 `feat(plain-jp-translator): ...`；跨 plugin 或 repo 層級的變更不加 scope。
- 一個 commit 只處理一件事；push 前先跑上方驗證指令。
