---
name: create-note
description: ちゃそまるの note 記事を、企画→調査→執筆→推敲→見出し画像・図解→コンプラチェックまで部隊で一式作る。「note を書いて」「note 記事を作って」と言われたときに使う。
argument-hint: <テーマ>（例: 指値と成行の違いを図解でじっくり）
---

# note 記事を作る

テーマ: $ARGUMENTS

あなたは編集長です。以下の順に部隊メンバー（サブエージェント）へ依頼し、成果物をつなげてください。各メンバーには記事フォルダのパスを必ず伝えること。

## 0. 準備
- 記事フォルダを作る: `content/articles/YYYY-MM-DD-<英小文字スラッグ>/`（日付は公開予定日。不明なら今日）
- テーマが空なら `content/ideas/` の最新の月間計画から次の未制作の記事を選ぶ。それもなければユーザーに聞く
- 無料記事か有料記事かを確認する（指定がなければ無料）

## 0.5 発信者キャラクターを決める
- ユーザーの指定があればそれを使う。指定がなければ `../brand/characters/README.md` の登録済みキャラを一覧で示して選んでもらう
- 未登録のキャラなら、先に `../brand/characters/_template.md` に沿って図鑑に登録してから進む
- 決まったキャラの ID を、以降すべてのメンバーへの依頼に含める

## 0.8 トレンド調査 → `note-researcher`
テーマまわりで伸びている発信を YouTube・X・ネット検索（最低2つ）で集めさせ、`research.md` を作成させる（記事は書かせない）。

## 1. 企画 → `note-strategist`
`research.md` を読ませたうえで `brief.md` を作成させる。Instagram の元投稿があればパスを伝える。

## 2. ファクトチェック → `note-researcher`
`fact-sheet.md` を作成させる。数字や制度を扱わない記事でも、主張の根拠を簡単に確認させる。

## 3. 執筆 → `note-writer`
`article.md` を作成させる。

## 4. 並行作業
- `note-editor`: 推敲と `edit.md`（タイトル案・タグ・導線）
- `note-designer`: 見出し画像・図解の `design.md`

## 5. コンプラチェック → `note-compliance-reviewer`
`review.md` を作成させる。
- **NG / 要修正** の場合: 指摘箇所を担当メンバーに修正させ（本文→`note-writer`、タイトル・タグ→`note-editor`、画像→`note-designer`）、再レビュー。OK になるまで繰り返す（最大3回。それでも OK にならなければユーザーに相談）

## 6. キャラクター図鑑を更新
`../brand/characters/README.md` の登場回数を +1 し、`../brand/characters/<id>/profile.md` の「登場した投稿」にこの記事フォルダ（`note作成部隊/content/articles/...`）を追記する。

## 7. ユーザーへの報告
- 判定、タイトル案、記事フォルダのパス、見出し画像の状況を短く報告する
- note への公開・Canva の書き出しは、ユーザーの明示的な確認を取ってから行う
