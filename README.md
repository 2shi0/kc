# Jekyll Blog (GitHub Pages)

Jekyll と GitHub Actions を利用して、GitHub Pages 上に自動公開するブログのテンプレートです。
ローカルマシンに Ruby が入っていなくても、GitHub へ push するだけで自動ビルド・デプロイされます。

---

## 🚀 公開までの簡単ステップ

### 1. GitHub 上で空のリポジトリを作成する
1. GitHub にログインし、[新しいリポジトリ (New repository)](https://github.com/new) を作成します。
   - **Repository name**: 任意の名前（例: `blog` または `<あなたのユーザー名>.github.io`）
   - **Public** を選択
   - 「Add a README file」などの初期化チェックは **付けない（空のまま）** で作成します。

### 2. ローカルリポジトリを GitHub に push する
作成したリポジトリの URL を使って、以下のコマンドを実行します。

```powershell
# 初回コミットを作成（まだコミットしていない場合）
git add .
git commit -m "feat: 初回ブログ基盤の作成"

# リモートリポジトリを追加（URLはご自身のリポジトリに変更してください）
git remote add origin https://github.com/<あなたのユーザー名>/<リポジトリ名>.git

# mainブランチへプッシュ
git push -u origin main
```

### 3. GitHub Pages のデプロイ設定を有効化する (重要!)
1. GitHub のリポジトリページを開きます。
2. 上部メニューの **Settings** をクリック。
3. 左サイドバーの **Pages** をクリック。
4. **Build and deployment** の **Source** プルダウンを「Deploy from a branch」から **「GitHub Actions」** に変更します。
5. 数分待つと、Actions のビルドが完了し、公開されたブログの URL が表示されます！
   - リポジトリ名が `<username>.github.io` の場合: `https://<username>.github.io/`
   - リポジトリ名が `blog` などの場合: `https://<username>.github.io/blog/`

---

## 📝 記事の書き方

新しい記事を追加するには、`_posts/` フォルダ内に新しい Markdown ファイルを作成します。

### ファイル名のルール
`YYYY-MM-DD-記事タイトル.markdown` (または `.md`)

例:
- `_posts/2026-11-15-my-first-post.markdown`

### 記事のフォーマット
ファイルの先頭に Front Matter（メタ情報）を記述します。

```markdown
---
layout: post
title: "記事のタイトル"
date: 2026-11-15 16:00:00 +0900
categories: [tech, web]
tags: [jekyll, markdown]
---

ここから本文を書きます。
Markdown記法がそのまま利用できます。
```

記事を書いて `git add` -> `git commit` -> `git push` すれば、自動的にブログに反映されます。

---

## ⚙️ サイトのカスタマイズ (`_config.yml`)

`_config.yml` を編集してサイト情報を変更できます。

- `title`: ブログのタイトル
- `email`: 連絡先メールアドレス
- `description`: サイトの説明文
- `author`: 著者情報（名前、GitHubアカウントなど）

---

## 💻 ローカルでプレビューしたい場合 (オプション)

ローカルでサイトをプレビューしながら書きたい場合は、Ruby (3.0以上) と Bundler をインストールし、以下を実行します：

```powershell
bundle install
bundle exec jekyll serve
```

ブラウザで `http://127.0.0.1:4000/` を開くとローカルプレビューが確認できます。
（※ローカル環境にRubyがない場合でも、GitHubにpushすればGitHub Actions側でビルドされるため、ローカルへのインストールは必須ではありません。）
