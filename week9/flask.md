# [Week9 Flask](https://cs50.jp/x/2022/week9/)

## Flask

### マイクロフレームワーク

- `app.py`
  - ここにWebアプリやその他のアプリケーションが置かれる
- `requirements.txt`
  - 使用したいライブラリを列挙する
- `static/`
  - ファイルもしくはディレクトリ
  - 画像、CSS、JavaScriptを格納する
- `templates/`
  - レンダリングするHTMLを格納する

### app.py

```python
from flask import Flask, render_template, request

app = Flask(__name__)

@app.route("/")
def index():
  # クエリパラメータを取得, 第二引数はdefaultValue
  name = request.args.get("name", "world")
  # 第一引数にレンダリングするHTMLを指定、第二引数はテンプレートに渡す変数を指定する
  return render_template("index.html", name=name)
```

```html
<div>Hello, {{ name }}</div>
```

### layout.html

- 共通化したレイアウトページ
- flaskのhtmlはJinja構文を使う

```html
<!DOCTYPE html>

<html lang="ja">
  <head>
    <meta name="viewport" content="initial-scale=1, width="device-width">
    <title>hello</title>
  </head>
  <body>
    {% block body %}{% endblock %}
  </body>
</html>
```

```html
{% extends "layout.html" %}

{% block body %}
  <div>...</div>
{% endblock %}
```

## MVC

### CONTROLLER

- ビジネスロジック
- 何をレンダリングするか、どんな値を表示するかなどすべての決定を行うコード
- `app.py`がこれに相当する

### VIEW

- ユーザーインタフェース
- `*.html`がこれに相当する

### MODEL

- 主にデータベース

## SQLite

```python
db = SQL("sqlite:///sample.db")

@app.route("/search")
def search():
  shows = db.execute("SELECT * FROM shows WHERE title = ?", "%" + request.args.get("q") + "%")
  return render_template("search.html", shows=shows)
```

- `sqlite://`
  - ローカルディレクトリを参照する慣習的な書き方
- `/sample.db`
  - 特定のディレクトリを指す

## Session

- ステートフルなアプリケーションを実装するために必要な技術

## JSON

- JavaScript Object Notation
- APIが返す一般的なフォーマット

## 感想

特定のフレームワークとデータベースを使ってアプリケーション作ろうぜという講義

目的はPythonやSQLをマスターすることではなく、異なる言語がどのように動作するかのメンタルモデルを構築することが大事

ログインアプリを作成する中で、同じ`route`で`GET`と`POST`の両方をサポートすることは物事を1つのURLに統合する方法として慣習的ということが理解できた

今までの実務経験でこの辺りは肌感でなんとなく認識していたものだけど改めて理解が深まった
