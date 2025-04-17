# <p align="center">🤖 302AI ブラウザユース MCP サーバー🚀✨</p>

<p align="center">自然言語によるブラウザー制御とWeb調査のためのモデルコンテキストプロトコル（MCP）を実装したAI駆動のブラウザー自動化サーバー。</p>

<p align="center"><a href="https://www.npmjs.com/package/@302ai/browser-use-mcp" target="blank"><img src="https://file.302.ai/gpt/imgs/github/20250102/72a57c4263944b73bf521830878ae39a.png" /></a></p >

<p align="center"><a href="README_zh.md">中文</a> | <a href="README.md">English</a> | <a href="README_ja.md">日本語</a></p>

![](docs/302_browser_use_mcp_jp.jpg) 

## インターフェースプレビュー
以下は使用例です
![](docs/302_browser_use_mcp_jp_screenshot_01.jpg)     

以下は利用可能なツールリストです
![](docs/302_browser_use_mcp_jp_screenshot_02.png)

   

## ✨ 機能特性 ✨
- 🔧 動的ローディング - リモートサーバーから自動的にツールリストを更新
- 🌐 複数のモードをサポート、ローカルで `stdin` モードを使用、またはリモートHTTPサーバーとしてホスト可能
### 🚀 ツールリスト
- [ブラウザ自動化タスクの作成](https://302ai-jp.apifox.cn/api-282236389)
- [ブラウザタスクのステータスを確認する](https://302ai-jp.apifox.cn/api-282236431)

## 開発

依存関係のインストール:

```bash
npm install
```

サーバーのビルド:

```bash
npm run build
```

開発用の自動再ビルド:

```bash
npm run watch
```

## インストール

Claude Desktopで使用するには、サーバー設定を追加してください:

MacOS系统: `~/Library/Application Support/Claude/claude_desktop_config.json`    
Windows系统: `%APPDATA%/Claude/claude_desktop_config.json`

```json
{
  "mcpServers": {
    "302ai-sandbox-mcp": {
      "command": "npx",
      "args": ["-y", "@302ai/browser-use-mcp"],
      "env": {
        "302AI_API_KEY": "YOUR_API_KEY_HERE"
      }
    }
  }
}
```

Cherry Studioで使用するには、サーバー設定を追加してください:

```json
{
  "mcpServers": {
    "Li2ZXXJkvhAALyKOFeO4N": {
      "name": "302ai-browser-use-mcp",
      "description": "",
      "isActive": true,
      "registryUrl": "",
      "command": "npx",
      "args": [
        "-y",
        "@302ai/browser-use-mcp"
      ],
      "env": {
        "302AI_API_KEY": "YOUR_API_KEY_HERE"
      }
    }
  }
}
```

ChatWiseで使用するには、以下の内容をクリップボードにコピーしてください
```json
{
  "mcpServers": {
    "302ai-sandbox-mcp": {
      "command": "npx",
      "args": ["-y", "@302ai/browser-use-mcp"],
      "env": {
        "302AI_API_KEY": "YOUR_API_KEY_HERE"
      }
    }
  }
}
```

設定->ツール->追加ボタン->クリップボードからインポートを選択
![](docs/302_browser_use_mcp_jp_screenshot_03.png)

### [ここ](https://dash.302.ai/apis/list)で302AI_API_KEYを取得してください
[使用チュートリアル](https://help.302.ai/jp/docs/API-guan-li)

### デバッグ

MCPサーバーは標準入出力(stdio)を介して通信するため、デバッグが難しい場合があります。パッケージスクリプトとして利用可能な[MCP Inspector](https://github.com/modelcontextprotocol/inspector)の使用をお勧めします:

```bash
npm run inspector
```

InspectorはブラウザでデバッグツールにアクセスするためのURLを提供します。

## ✨ 302.AIについて ✨
[302.AI](https://302.ai/ja/)は企業向けのAIアプリケーションプラットフォームであり、必要に応じて支払い、すぐに使用できるオープンソースのエコシステムです。✨
1. 🧠 言語モデル、画像モデル、音声モデル、動画モデルなど、最新かつ包括的なAI機能とブランドを集約
2. 🚀 基本モデルの上に深層アプリケーション開発を行い、単なるチャットボットではなく、真のAI製品を開発
3. 💰 月額料金なし、すべての機能を従量課金制で提供し、参入障壁を低く、可能性を高く
4. 🛠 チームや中小企業向けの強力な管理バックエンド、一人で管理し、多人数で利用可能
5. 🔗 すべてのAI機能にAPIアクセスを提供し、すべてのツールをオープンソースでカスタマイズ可能（進行中）
6. 💡 強力な開発チームが週に2-3個の新アプリケーションをリリース、製品は毎日更新。開発者の参加も歓迎