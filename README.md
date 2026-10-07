# note-company

開発した作品と、その過程で起きたことを note 記事に変える「AI編集部」です。
Claude Code のサブエージェントを部署に見立て、企画 → 取材 → 執筆 → 校閲 → 公開準備までを進めます。

## 組織

| 部署 | エージェント | 役割 |
|---|---|---|
| 編集長 | `editor-in-chief` | 工程管理・企画の優先順位付け・最終チェック |
| 企画部 | `planner` | ネタ出し、読者設定、タイトル案、記事の目的（集客/販売）判定 |
| 取材部 | `researcher` | GitHubの README・コミット履歴・コードから事実を抽出し、社長への質問を作る |
| 執筆部 | `writer` | 文体ガイドに沿って本文を書く |
| 校閲部 | `proofreader` | 事実確認・機密情報チェック・AIっぽさの除去 |
| 販売部 | `marketer` | タグ、見出し画像案、X告知文、ココナラ・ポートフォリオへの導線 |

社長（あなた）の出番は **企画の承認** と **取材質問への回答** の2か所です。

## 使い方

```
/article-plan                 # 企画部がネタを5案出す → 1つ選ぶ
/article-research <slug>      # 取材メモと質問リストを作る → answers.md に回答する
/article-write <slug>         # 執筆 → 校閲（不合格なら最大2回書き直し）
/article-publish <slug>       # note に貼る用の公開パッケージを出力
```

## フォルダ構成

```
CLAUDE.md            全社ルール
.claude/agents/      社員（サブエージェント）定義
.claude/commands/    制作フローのコマンド
company/             会社の資産（プロフィール・戦略・文体・作品・サービス・読者）
templates/           記事の型
articles/<日付_slug>/ 1記事1フォルダ（01_plan → 05_publish）
backlog.md           ネタ帳
```

## 最初にやること

1. `company/services.md` にココナラ3サービスの内容を貼る
2. `company/profile.md` の【要記入】を埋める
3. 既存の note 記事や X 投稿があれば `company/style-guide.md` の「見本」に貼る
4. `/article-plan` を実行
