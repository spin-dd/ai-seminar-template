# AI と作業するリポジトリのテンプレート

Claude などの AI に作業を委任するリポジトリの、最小の構成です。

| ファイル | 役割 |
|---|---|
| `AGENTS.md` | AI がセッションの開始時に読み込むルール |
| `.claude/skills/retro/SKILL.md` | 振り返りのスキル。`/retro` で起動する |

## 使用方法

1. 「Use this template」から、自分のリポジトリを作成する。
2. AI に作業を依頼する。指摘を繰り返した場合は、`AGENTS.md` にルールを追加する。
3. セッションの終了の前に `/retro` を実行し、提案されたスキルとルールを採用する。

## ライセンス

振り返りのスキルは、[mattpocock/skills](https://github.com/mattpocock/skills) の retro（MIT License）を基に作成しています。
