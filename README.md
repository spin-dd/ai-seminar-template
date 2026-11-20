# AI と作業するリポジトリのテンプレート

Claude などの AI に作業を委任するリポジトリの、最小の構成です。

| ファイル | 役割 |
|---|---|
| `AGENTS.md` | AI がセッションの開始時に読み込むルール |
| `.agents/skills/retro/SKILL.md` | 振り返りのスキル。`/retro` で起動する |
| `.claude/skills` | `.agents/skills` へのリンク。Claude がスキルを参照する場所 |

## 使用方法

1. 「Use this template」から、自分のリポジトリを作成する。
2. AI に作業を依頼する。指摘を繰り返した場合は、`AGENTS.md` にルールを追加する。
3. セッションの終了の前に `/retro` を実行し、提案されたスキルとルールを採用する。

## スキルの追加

スキルの管理のツールは複数あります（`npx skills` など）。このテンプレートは [APM](https://github.com/microsoft/apm) を使用します。APM は、他者が公開したスキルを、特定のバージョンに固定して管理します。

`apm.yml` に、[mattpocock/skills](https://github.com/mattpocock/skills)（MIT License）の汎用のスキルを、バージョンを固定して登録しています。

| スキル | 内容 |
|---|---|
| `grilling`、`grill-me` | 計画を質問で詳細化する |
| `grill-with-docs`、`domain-modeling` | 用語と決定を文書に記録しながら、計画を詳細化する |
| `to-spec`、`to-tickets` | 会話の内容から仕様を作成し、Issue に分割する |
| `setup-matt-pocock-skills` | `to-spec` と `to-tickets` が使用する設定を作成する |

導入する場合は、AI に「microsoft/apm を導入して、apm.yml のスキルを導入してください」と依頼します。スキルは `.agents/skills/` に配置されます。

スキルを追加する場合は、AI に「○○ のスキルを apm.yml に追加してください」と依頼します。

## ライセンス

振り返りのスキルは、[mattpocock/skills](https://github.com/mattpocock/skills) の retro（MIT License）を基に作成しています。
