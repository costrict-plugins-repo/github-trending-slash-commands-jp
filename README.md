# slash-commands-jp

> A Claude Code plugin that fetches the **latest official slash-command list** on every invocation and renders it in **Japanese, by category, with one-line real-world usage examples**.

[English](#english) | [日本語](#日本語)

---

## English

### What it does

- Run `/slash-commands-jp:list` and get the entire Claude Code slash command catalog rendered in Japanese, grouped by category, with one-line usage examples for each command.
- The plugin fetches the official docs at https://code.claude.com/docs/en/commands.md on every run, so it tracks newly added and deprecated commands automatically.

### Why this exists

The Claude Code command surface is large (80+ commands), official docs are English-only, and `/help` alone gives poor at-a-glance coverage. For Japanese users who are mid-funnel — past "what is Claude Code" but not yet fluent in every command — there was no single screen that combined: latest, categorized, Japanese, and "what would I actually use this for?". This plugin is that screen.

### Installation

#### From the official marketplace (in review)

```
/plugin install slash-commands-jp
```

#### Directly from GitHub

```bash
git clone https://github.com/keitashimoda24-maker/slash-commands-jp.git \
  ~/.claude/plugins/slash-commands-jp
```

Then run `/reload-plugins` in Claude Code.

### Usage

```
/slash-commands-jp:list
```

Output is grouped into ~15 categories (session management / context & memory / model & exec control / planning & review / automation & parallelism / diagnostics / settings & UI / integration / etc.), with deprecated commands separated.

### Features

- **Always current** — WebFetch on every invocation
- **Japanese surface** — category names, descriptions, and usage examples all localized
- **Operational usage examples** — one-line "when would I actually use this"
- **Complete coverage** — no omissions, deprecated commands listed separately
- **Explicit invocation only** — `disable-model-invocation: true` so the model never auto-triggers it

---

## 日本語

### 何ができる？

- `/slash-commands-jp:list` を実行するだけで、Claude Code の全コマンドが日本語で一覧表示されます
- 公式ドキュメント（https://code.claude.com/docs/en/commands.md）から毎回最新版を取得するため、新機能の追加や廃止に自動追従します
- 各コマンドに「どんな業務シーンで使うか」の具体例を1行つけて表示するので、初心者でも即座に活用イメージが湧きます

### なぜ作ったか

Claude Code は公式ドキュメントが英語のみで、コマンド数も多く（80以上）、初心者には全体像の把握が困難です。

- `/help` だけだと一覧性が低い
- 公式ドキュメントは英語＋抽象的な説明だけ
- バージョンアップで増減するコマンドを追いきれない

→ このプラグインは「日本語 × カテゴリ別 × 業務実例 × 自動最新化」を1コマンドで実現します。

### インストール

#### 公式マーケットから（レビュー待ち）

```
/plugin install slash-commands-jp
```

#### GitHub から直接

```bash
git clone https://github.com/keitashimoda24-maker/slash-commands-jp.git \
  ~/.claude/plugins/slash-commands-jp
```

その後 Claude Code で `/reload-plugins` を実行。

### 使い方

```
/slash-commands-jp:list
```

公式ドキュメントから最新コマンド一覧を取得し、以下のカテゴリで日本語整理して表示します:

1. ワークフロー別ショートガイド
2. セッション管理
3. コンテキスト・メモリ
4. モデル・実行制御
5. 計画・レビュー
6. 自動化・並列実行
7. 診断・トラブル
8. 設定・UI
9. 連携・拡張
10. 情報・分析
11. ファイル・出力
12. モバイル・デスクトップ
13. クラウド・リモート環境
14. その他・特殊
15. 廃止済み（あれば）

### 特徴

- **自動最新化** - WebFetch で毎回公式から取得
- **日本語表示** - カテゴリ名・説明・実用例すべて日本語
- **業務実例つき** - 各コマンドに「どんな時に使うか」を1行で
- **網羅性** - 省略なし、廃止コマンドも別セクションで表示
- **モデル自動起動なし** - `disable-model-invocation: true` で明示呼び出し限定

---

## Author

[@keitashimoda24-maker](https://github.com/keitashimoda24-maker)

Non-engineer area manager running 10 convenience stores in Japan, building daily automation with Claude Code (30+ systems and counting).

## Related Projects

- [claude-code-smart-hooks](https://github.com/keitashimoda24-maker/claude-code-smart-hooks) — Conditional ultrathink injection for consistent reasoning depth
- [devils-advocate](https://github.com/keitashimoda24-maker/devils-advocate) — Devil's advocate agent for plan/design review
- [mac-pixel-bridge](https://github.com/keitashimoda24-maker/mac-pixel-bridge) — Resilient ADB clipboard / screenshot bridge

## License

MIT — see [LICENSE](LICENSE).
