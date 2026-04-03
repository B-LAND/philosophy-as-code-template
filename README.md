# Philosophy as Code

**Why Before How in AI Agent Governance**

Define *why* before *how*. Codify your organization's philosophy as a three-layer structure, and let AI agents derive decisions from principles — not just rules.

*why* を *how* より先に定義せよ。組織の哲学を3層構造としてコード化し、AIエージェントがルールではなく原理原則から判断を導出できるようにする。

---

## Quick Start

1. Copy this template into your project root / このテンプレートをプロジェクトルートにコピー
2. Fill in the blanks in `CLAUDE.md` / `CLAUDE.md` の空欄を埋める
3. Customize the rules in `.claude/rules/` / `.claude/rules/` をカスタマイズ

That's it. Your AI agent now has a philosophy.
これだけで、AIエージェントに哲学が入る。

---

## Directory Structure / ディレクトリ構成

```
your-project/
|
|-- CLAUDE.md                      # Philosophy definition / 哲学の定義（憲法）
|
|-- .claude/
|   |-- rules/                     # Harness control layer / ハーネス制御層（法律）
|   |   |-- philosophy-first.md    # [always injected / 常時注入]
|   |   |-- code-standards.md      # [code edit only / コード編集時のみ]
|   |   +-- (add your own)         # [target paths / 対象パス指定]
|   |
|   +-- skills/                    # Domain knowledge / ドメイン知識（判例）
|       |-- <skill-name>/
|       |   +-- SKILL.md           # Loaded on invoke / 呼び出し時のみ読み込み
|       +-- ...
```

---

## CLAUDE.md — The Three-Layer Philosophy / 3層哲学

CLAUDE.md defines your organization's philosophy in three layers:

CLAUDE.mdは組織の哲学を3層で定義する：

**Layer 1: Principles / 原理原則** — Structural facts. Immutable. / 構造的事実。不変。

> "Methods alone cannot handle the unknown."
> 「メソッドだけでは未知に対応できない」

**Layer 2: Values / 理念** — Chosen priorities. Your organization's will. / 選択された優先順位。組織の意志。

> "Define philosophy before selecting methodology."
> 「手法やツールの選定より先に哲学を定義する」

**Layer 3: Thinking Patterns / 思考の型** — Decision derivation procedures. / 判断導出の手順。

> "Ask why before how. Define correctness before implementation."
> 「なぜを先に問う。正しさを先に定義する」

Any output that does not pass the philosophy is not shipped — just as code that fails its tests is not shipped.

哲学を通過しない出力は出荷しない ── テストを通過しないコードを出荷しないのと同じように。

---

## Rules — Context Injection Control / コンテキスト注入制御

Rules in `.claude/rules/` translate philosophy into operational guidelines. Each rule uses a `paths` field to control *when* it is injected:

`.claude/rules/` のルールは哲学を運用指針に変換する。`paths` フィールドで注入タイミングを制御：

```yaml
---
# No paths = always injected / pathsなし = 常時注入
---
```

```yaml
---
paths:
  - "**/*.py"
  - "**/*.js"
# Injected only when editing code / コード編集時のみ注入
---
```

The agent maintains philosophical awareness at all times while receiving context-appropriate rules only when relevant.

エージェントは常に哲学を意識しつつ、文脈に応じたルールだけを受け取る。コンテキストウィンドウを無駄にしない。

---

## Skills — Domain Knowledge / ドメイン知識

Skills in `.claude/skills/` are loaded only when invoked. They hold domain knowledge derived from the philosophy.

`.claude/skills/` のスキルは呼び出し時のみ読み込まれる。哲学から導出されたドメイン知識を保管する。

1. Create: `.claude/skills/your-skill-name/SKILL.md`
2. Invoke: `/your-skill-name`

Skills can grow without consuming context. / スキルを増やしてもコンテキストを消費しない。

---

## How It Works / 動作フロー

```
1. PLANNING      — Consult CLAUDE.md. "Which value does this task serve?"
   計画            CLAUDE.mdを参照。「このタスクはどの理念に紐づくか？」
       |
       v
2. EXECUTION     — AI agent works under philosophical guidance.
   実行            CLAUDE.md (always) + Rules (auto-inject) + Skills (on invoke)
       |
       v
3. REVIEW        — Verify against philosophy. Pass = ship. Fail = revise.
   検証            哲学に照らして検証。合格 = 出荷。不合格 = 修正。
       |
       v
4. RETROSPECTIVE — Verify the philosophy itself. Evolve if warranted.
   振り返り         哲学自体を検証。原理原則は変えない。理念・思考の型は進化しうる。
```

---

## Whitepaper / ホワイトペーパー

Why this exists. Why harnesses without philosophy ritualize. A case study of before/after deployment.

哲学なきハーネスがなぜ形骸化するか、導入前後のケーススタディを含む全文：

- [English (web)](https://philosophy-as-code.b-land.co/whitepaper/en/) / [English (markdown)](docs/whitepaper-en.md)
- [Japanese / 日本語 (web)](https://philosophy-as-code.b-land.co/whitepaper/ja/) / [日本語 (markdown)](docs/whitepaper-ja.md)

---

## License

MIT

---

Built by [B-LAND Inc.](https://philosophy-as-code.b-land.co/)
