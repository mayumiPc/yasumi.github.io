# yasumi模擬店MTG議事録サイト

yasumi模擬店の会議議事録を共有するGitHub Pagesサイトです。

## 概要

このサイトは、Jekyllを使用して構築された静的サイトで、yasumi模擬店の会議議事録をMarkdownファイル形式で管理・公開しています。

## 機能

- 📝 議事録の一覧表示
- 📅 日付順での議事録整理
- 🔍 参加者、場所などのメタ情報表示
- 📱 レスポンシブデザイン対応
- 🎨 モダンで見やすいUI

## サイト構成

```
yasumi.github.io/
├── _config.yml          # Jekyll設定ファイル
├── Gemfile              # Ruby依存関係
├── index.html           # トップページ
├── meetings.html        # 議事録一覧ページ
├── _layouts/            # レイアウトテンプレート
│   ├── default.html     # デフォルトレイアウト
│   └── meeting.html     # 議事録専用レイアウト
├── _meetings/           # 議事録ファイル（Markdown）
│   └── *.md            # 議事録ファイル
└── assets/
    └── css/
        └── style.css    # スタイルシート
```

## 議事録の追加方法

### 1. 新しい議事録ファイルを作成

`_meetings/`ディレクトリに新しいMarkdownファイルを作成します。

ファイル名の例: `2024-01-15-kickoff-meeting.md`

### 2. フロントマターを記述

ファイルの先頭に以下のメタ情報を記述します：

```yaml
---
layout: meeting
title: "会議タイトル"
date: 2024-01-15
participants: ["参加者1", "参加者2", "参加者3"]
location: "会議場所"
excerpt: "議事録の概要（省略可）"
---
```

### 3. 議事録の内容を記述

Markdown形式で議事録の内容を記述します：

```markdown
# 会議タイトル

## 会議概要
- **日時**: 2024年1月15日 19:00-21:00
- **参加者**: 参加者1、参加者2、参加者3
- **場所**: 会議場所
- **議題**: 議題の概要

## 決定事項
### 1. 決定事項1
- 詳細1
- 詳細2

## 次回会議予定
- **日時**: 2024年1月22日 19:00-21:00
- **議題**: 次回の議題

## アクションアイテム
- [ ] タスク1: 担当者名
- [ ] タスク2: 担当者名

## 備考
- その他の注意事項
```

## ローカルでの開発

### 必要な環境
- Ruby 2.7以上
- Bundler

### セットアップ手順

1. リポジトリをクローン
```bash
git clone https://github.com/yasumi/yasumi.github.io.git
cd yasumi.github.io
```

2. 依存関係をインストール
```bash
bundle install
```

3. ローカルサーバーを起動
```bash
bundle exec jekyll serve
```

4. ブラウザで `http://localhost:4000` にアクセス

## デプロイ

このサイトはGitHub Pagesで自動的にデプロイされます。

1. 変更をコミットしてプッシュ
```bash
git add .
git commit -m "議事録を追加"
git push origin main
```

2. GitHub Pagesの設定で、Sourceを「Deploy from a branch」に設定し、Branchを「main」に設定

3. 数分後に `https://yasumi.github.io` でサイトが公開されます

## カスタマイズ

### サイト情報の変更

`_config.yml`ファイルで以下の項目を変更できます：

- `title`: サイトタイトル
- `description`: サイトの説明
- `author`: 作成者名
- `url`: サイトのURL

### スタイルの変更

`assets/css/style.css`を編集してデザインをカスタマイズできます。

## 注意事項

- 議事録ファイルは必ず`_meetings/`ディレクトリに配置してください
- ファイル名は日付を含む形式（例：`YYYY-MM-DD-会議名.md`）にしてください
- フロントマターの`date`フィールドは必須です
- 機密情報は含めないよう注意してください

## ライセンス

このプロジェクトはMITライセンスの下で公開されています。

## お問い合わせ

ご質問やご要望がございましたら、GitHubのIssuesページまでお気軽にお声がけください。 