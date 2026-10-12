---
name: plan-notes
description: ちゃそまるの note 記事の1か月分の計画（テーマ、柱、公開日、元ネタ、無料/有料候補）を立てる。「note の企画を立てて」「来月の note 計画を作って」と言われたときに使う。
argument-hint: [YYYY-MM]（省略時は来月）
---

# note の月間計画を作る

対象月: $ARGUMENTS（空なら来月）

0. `note-researcher` に、柱ごとに伸びている発信のトレンド調査をさせ、`content/ideas/research-YYYY-MM-DD-<スラッグ>.md` に保存させる
1. `note-strategist` に、トレンド調査を読ませたうえで対象月の計画 `content/ideas/YYYY-MM.md` を作らせる
   - 本数の目安: 月4本（週1本）。ユーザーの指定があればそれに従う
   - 柱の比率は `../brand/brand-guide.md` に合わせる
   - Instagram の既存投稿（`../content/`）から深掘り候補を最低1本入れる
   - 有料候補があれば理由とともに明記（決定はユーザー）
2. 採用しなかったネタは `content/ideas/backlog.md` に追記させる
3. 計画の表をユーザーに示し、修正したい点・キャラの指定を確認する
