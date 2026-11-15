---
layout: post
title: "Jekyllへようこそ！ブログをはじめました"
date: 2026-11-15 16:00:00 +0900
categories: [blog, tech]
tags: [jekyll, github-pages, markdown]
---

JekyllとGitHub Pagesを利用して、技術ブログを開設しました！

## Jekyllで記事を書く方法

記事は `_posts/` ディレクトリの中に `YYYY-MM-DD-記事タイトル.markdown` という命名規則でファイルを作成して執筆します。

### Front Matter（記事のメタ情報）
各Markdownファイルの先頭には、以下のようにハイフン3つで囲まれた「Front Matter」を記述します。

```yaml
---
layout: post
title: "記事のタイトル"
date: 2026-11-15 16:00:00 +0900
categories: [カテゴリー名]
tags: [タグ1, タグ2]
---
```

### コードブロックのハイライト

Jekyllではコードのシンタックスハイライトが標準でサポートされています。

```python
def greet(name: str) -> str:
    return f"Hello, {name}! Welcome to my blog."

print(greet("World"))
```

### GitHubへの公開

記事を書いてコミットし、GitHubのリポジトリへ `git push` すれば、GitHub Actionsが自動的にブログをビルド・公開してくれます！
