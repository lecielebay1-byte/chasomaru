---
name: review-insights
description: 過去のInstagram投稿のインサイトを分析し、伸びた型と次の企画への改善提案をまとめる。「数字を振り返って」「分析して」と言われたときに使う。
argument-hint: [期間]（例: 直近30日）
---

# インサイトを振り返る

期間: $ARGUMENTS（指定がなければ直近30日）

1. `analytics-analyst` に分析を依頼する
   - Windsor.ai の Instagram 接続があればそこから取得
   - なければ、ユーザーにインサイト画面のスクリーンショットか CSV を `content/reports/raw/` に置いてもらうよう依頼する
2. 出力: `content/reports/YYYY-MM-DD.md`
3. 提案された企画案は `content-strategist` に渡し、`content/ideas/backlog.md` に追加させる
4. ユーザーに、サマリー3行と「次にやること」を伝える
