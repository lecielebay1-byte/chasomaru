# note 作成部隊（ちゃそまる用）

ちゃそまる｜ゼロから始めるやさしい株式投資 の **note 記事** を、Claude Code の部隊（サブエージェント）で作るための専用作業場です。
Instagram 用の制作部隊（親フォルダ）とは別に動きますが、ブランドガイド・コンプラルール・キャラクター図鑑は共通です。

## 使い方

1. Claude Code で **このフォルダ（`note作成部隊/`）を開く**
2. コマンドを入力する

| コマンド | 内容 |
|---|---|
| `/plan-notes` | 1か月分の note 記事計画を作る |
| `/create-note 指値と成行の違いを図解でじっくり` | note 記事を一式作る |

キャラは記事ごとに指定します（例: `/create-note 株価が動く理由 キャラはちゃそまる`）。

## 部隊の構成

```
                 編集長（メインの Claude）
                          │
  ┌───────────┬───────────┼───────────┬───────────┐
企画担当     リサーチャー   ライター     編集担当     デザイナー
note-        note-         note-        note-        note-
strategist   researcher    writer       editor       designer
                          │
             コンプラ・レビュアー（公開前の最終関門）
             note-compliance-reviewer
```

## フォルダ構成

```
note作成部隊/
  CLAUDE.md          編集長ルール
  brand/
    note-guide.md    note 独自の書き方・型・有料記事の注意
    note-specs.md    note の仕様（見出し画像サイズなど）
  templates/         ブリーフ・記事原稿のテンプレート
  content/
    ideas/           月間計画（YYYY-MM.md）とネタ帳（backlog.md）
    articles/        記事ごとのフォルダ（YYYY-MM-DD-slug/）
    reports/         note の数字の振り返り
  .claude/agents/    部隊メンバーの定義
  .claude/skills/    制作フロー（/create-note など）

（共有：親フォルダ）
../brand/brand-guide.md   ブランドガイド
../brand/compliance.md    コンプラルール
../brand/characters/      キャラクター図鑑
```

1記事のフォルダには `research.md` → `brief.md` → `fact-sheet.md` → `outline.md` → `article.md` → `edit.md` → `design.md` → `review.md` が順にたまっていきます。
完成稿は `article.md`（note にそのまま貼れる形）です。

## 大事なルール

- 個別銘柄の売買推奨・「必ず儲かる」などの断定はしない（`../brand/compliance.md`）
- 公開前に必ずコンプラ・レビューを通す
- note への投稿や Canva の書き出しは、あなたが確認してから行う
- 有料記事にする場合は、企画の段階で相談する
