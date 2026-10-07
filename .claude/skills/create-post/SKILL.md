---
name: create-post
description: 投資初心者向けInstagramの画像（カルーセル）投稿を、企画→調査→原稿→デザイン→キャプション→コンプラチェックまで部隊で一式作る。「画像投稿を作って」「カルーセルを作って」と言われたときに使う。
argument-hint: <テーマ>（例: NISAとiDeCoの違い）
---

# 画像（カルーセル）投稿を作る

テーマ: $ARGUMENTS

あなたは編集長です。以下の順に部隊メンバー（サブエージェント）へ依頼し、成果物をつなげてください。各メンバーには投稿フォルダのパスを必ず伝えること。

## 0. 準備
- 投稿フォルダを作る: `content/posts/YYYY-MM-DD-<英小文字スラッグ>/`（日付は公開予定日。不明なら今日）
- テーマが空なら `content/ideas/` の最新週間計画から次の未制作の画像投稿を選ぶ。それもなければユーザーに聞く

## 0.5 発信者キャラクターを決める
- ユーザーの指定があればそれを使う。指定がなければ `brand/characters/README.md` の登録済みキャラを一覧で示してユーザーに選んでもらう
- 指定されたキャラが未登録なら、先に `/add-character` の手順で図鑑に登録してから進む
- 決まったキャラの ID を、以降すべてのメンバーへの依頼に含める

## 1. 企画 → `content-strategist`
テーマから `brief.md` を作成させる。

## 2. 調査 → `researcher`
`brief.md` を読ませ、`fact-sheet.md` を作成させる。数字や制度を一切扱わない投稿（マインド系など）でも、主張の根拠を簡単に確認させる。

## 3. 原稿 → `carousel-writer`
`carousel.md` を作成させる。

## 4. 並行作業
- `visual-designer`: `carousel.md` から Canva デザイン（または指示書）を作り `design.md` に記録
- `caption-writer`: `caption.md` を作成

## 5. コンプラチェック → `compliance-reviewer`
`review.md` を作成させる。
- **NG / 要修正** の場合: 指摘箇所を担当メンバーに修正させ（原稿→`carousel-writer`、キャプション→`caption-writer`、デザイン→`visual-designer`）、再度レビュー。OK になるまで繰り返す（最大3回。それでも OK にならなければユーザーに相談）

## 6. キャラクター図鑑を更新
`brand/characters/README.md` の登場回数を +1 し、`brand/characters/<id>/profile.md` の「登場した投稿」にこの投稿フォルダを追記する。制作中にキャラの新しいポーズ・口癖・素材が生まれたら profile.md に追記する。

## 7. 報告
ユーザーに以下を簡潔に伝える:
- 表紙タイトルと構成（スライド数）
- Canva デザインの URL（あれば）
- キャプション冒頭
- レビュー結果と、修正した点
- 公開前にユーザー自身が確認すべきこと

Instagram への投稿や Canva デザインの書き出しは、ユーザーが明示的に頼むまで行わない。
