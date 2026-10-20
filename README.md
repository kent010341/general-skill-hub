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
