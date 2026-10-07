# ちゃそまる Instagram 制作部隊

投資初心者向け Instagram アカウントのリール・画像投稿を、Claude Code の「部隊」（サブエージェント）で作るためのリポジトリです。

## 部隊の構成

```
                    編集長（メインの Claude）
                             │
  ┌──────────┬──────────┬────┴─────┬──────────┬──────────┐
企画担当    リサーチャー  ライター     デザイナー  キャプション  アナリスト
strategist  researcher   carousel /   visual-     caption-     analytics-
                         reel-script  designer    writer       analyst
                             │
                   コンプラ・レビュアー（公開前の最終関門）
```

| メンバー | やること |
|---|---|
| content-strategist | ネタ出し、週間カレンダー、投稿ブリーフ |
| researcher | NISA・iDeCo・税金などを一次情報で調べて出典付きファクトシートに |
| carousel-writer | 画像投稿のスライド構成とコピー |
| reel-scriptwriter | リール台本（フック・カット割り・テロップ・ナレーション） |
| visual-designer | Canva でデザイン作成（Canva 未接続ならデザイン指示書） |
| caption-writer | キャプション・ハッシュタグ・固定コメント |
| compliance-reviewer | 金融商品取引法・ステマ規制などの観点で公開前チェック |
| analytics-analyst | インサイト分析（Windsor.ai 接続時は自動取得） |

## 使い方

Claude Code でこのリポジトリを開き、次のコマンドを入力します。

| コマンド | 内容 |
|---|---|
| `/plan-week` | 1週間分の投稿計画を作る |
| `/create-post NISAとiDeCoの違い` | 画像（カルーセル）投稿を一式作る |
| `/create-reel 複利ってなに？を30秒で` | リールを一式作る |
| `/review-insights` | 過去投稿の数字を振り返る |

特定のメンバーに直接頼むこともできます（例:「researcher に新NISAの最新の非課税枠を調べさせて」）。

## 最初にやること

1. `brand/brand-guide.md` の `【要記入】` を埋める（アカウント名、キャラ、色、フォント、語尾）
2. （任意）Canva にブランドキット / ブランドテンプレートを作っておくと、デザインの統一感が上がります
3. （任意）Windsor.ai で Instagram を接続すると、分析を自動化できます

## フォルダ構成

```
brand/            ブランドガイド・コンプラルール・Instagram 仕様
templates/        ブリーフ・カルーセル・リール台本のテンプレート
content/
  ideas/          週間計画（YYYY-Www.md）とネタ帳（backlog.md）
  posts/          画像投稿ごとのフォルダ（YYYY-MM-DD-slug/）
  reels/          リールごとのフォルダ（YYYY-MM-DD-slug/）
  reports/        分析レポート
.claude/agents/   部隊メンバーの定義
.claude/skills/   制作フロー（/create-post など）
```

1投稿のフォルダには `brief.md` → `fact-sheet.md` → `carousel.md` or `reel-script.md` → `design.md` → `caption.md` → `review.md` が順にたまっていきます。

## 大事なルール

- 個別銘柄の売買推奨・「必ず儲かる」などの断定はしない（詳しくは `brand/compliance.md`）
- 公開前に必ずコンプラ・レビューを通す
- Instagram への投稿や Canva の書き出しは、あなたが確認してから行う
