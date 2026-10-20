# general-skill-hub
AI Agent Skill Hub for General Usage

## 安裝

在 Claude Code 中加入本 marketplace：

```
/plugin marketplace add Kent010341/general-skill-hub
```

再安裝需要的 plugin：

```
/plugin install plain-jp-translator@general-skill-hub
```

## 目錄結構

```
.claude-plugin/marketplace.json        # marketplace 清單
plugins/<plugin>/.claude-plugin/plugin.json
plugins/<plugin>/skills/<skill>/SKILL.md
```

每個 skill 各自是一個 plugin，可單獨安裝。

## Plugins

| Plugin | 說明 | 使用方式 |
| --- | --- | --- |
| plain-jp-translator | 將中文或英文委託文翻譯成自然、淺白的日文委託文 | `/plain-jp-translator:plain-jp-translator <委託文>`（僅手動呼叫） |
| hallway-tester | 以一般使用者的經驗直覺測試介面，找出需要停下來思考的可用性風險 | `/hallway-tester:hallway-tester`（僅手動呼叫） |
| lottery-stock-scanner | 探索高度不確定、尚未被市場充分定價的彩券型股票（非投資建議） | `/lottery-stock-scanner:lottery-stock-scanner`（僅手動呼叫） |
| oc-namer | 根據角色設定跨語言創作英文拼寫的 OC 名字，附語源、音韻設計與 IPA | `/oc-namer:oc-namer`（僅手動呼叫） |
| precision-editor | 不改原意、不重寫全文的文字潤稿，附修改理由 | `/precision-editor:precision-editor`（僅手動呼叫） |
