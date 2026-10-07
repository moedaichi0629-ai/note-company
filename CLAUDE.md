# note-company 全社ルール

このリポジトリは、社長（リポジトリ所有者）の開発実績を note 記事にする編集部です。
記事制作は `.claude/commands/` の4つのコマンドで進め、各工程は `.claude/agents/` の担当エージェントに任せます。

## 現在のフェーズ：集客期

`company/strategy.md` を必ず参照すること。いまは **「AI受託開発者としての集客」が最優先** で、有料記事は例外扱い。
- 記事の目的は「読んだ店舗オーナー・個人事業主が、この人に頼めそうだと思うこと」
- 記事末尾の導線はココナラのサービスページかポートフォリオ
- フェーズの切り替え条件は strategy.md に書いてある。勝手に販売期の方針で企画しない

## 絶対に守ること

1. **事実は一次情報からのみ書く。** 一次情報とは、作品リポジトリの README・コード・コミット履歴、`company/` の資料、記事フォルダの `answers.md`（社長の回答）。ここにない数字・成果・感想・エピソードを作らない。足りなければ質問にする
2. **機密を出さない。** APIキー、トークン、環境変数の値、顧客名・店舗名、案件の金額、クライアントとのやりとりの原文は書かない。必要なら「美容室A」のように伏せる
3. **AIっぽい文章にしない。** 詳細は `company/style-guide.md`
4. **できていないことを、できると書かない。** README に「廃止」「未実装」とある機能は紹介しない
5. 記事1本につき、ココナラまたはポートフォリオへの導線は1か所（本文の流れに合う位置）

## 記事フォルダの約束

`articles/YYYY-MM-DD_slug/` に以下を置く。前工程のファイルは上書きせず、修正は次の番号のファイルに書く。

| ファイル | 作成者 |
|---|---|
| `01_plan.md` | planner |
| `02_research.md` | researcher |
| `answers.md` | 社長 |
| `03_draft.md` | writer |
| `04_review.md` | proofreader |
| `05_publish.md` | marketer |

## 参照する資料

- `company/strategy.md` 発信方針とフェーズ
- `company/profile.md` 社長の経歴・強み
- `company/products.md` 作品一覧とリポジトリURL
- `company/services.md` ココナラのサービス
- `company/persona.md` 想定読者
- `company/style-guide.md` 文体
- `templates/` 記事の型
