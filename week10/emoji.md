# [Week10 Emoji](https://cs50.jp/x/2022/week10/)

## クイズ形式の振り返りテスト

- CSSとは何の略か？
  - Cascading Style Sheet⭕️
- コンパイラの役割を最もよく表しているものは何か？
  - ソースコードをマシンコードに変換する⭕️
- argcの型は何か？
  - int⭕️
- C言語で型の異なる複数の変数を1つの新しい型に結合するにはどうすれば良いか？
  - Structs⭕️
- Pythonに関する記述のうち、誤っているものはどれか？
  - Pythonの配列は固定サイズである⭕️
- C言語でstrcmpは何を返すか？
  - boolean❌
    - 正解 → integer⭕️
- ソートされていないアイテムのリストがあります。検索のために事前にアイテムをソートすべきか？
  - リストを何度も検索するのであれば最初にソートすべき⭕️
- `CREATE INDEX`コマンドをSQLで実行した時、どのようなタイプのデータ構造を作成しますか？
  - B-trees⭕️
- SQLインジェクション攻撃の例はどれか？
  - 誰かがウェブフォームから悪意のあるSQLコマンドを送信した⭕️
- 配列の要素はどのようにしてメモリに格納されているか？
  - たまたま利用可能なランダムな場所❌
    - これはヒープのmallocの説明
    - 正解 → 連続して⭕️
- 映画スターのテーブルから、ZendayaのIDを選択するSQLクエリはどれか？
  - `SELECT id FROM moviestars WHERE name = ‘Zendaya'`⭕️

## Emoji

- 絵文字は日本から始まった
  - 1999年にドコモから発表された
- 絵文字には日本の食べ物がたくさん含まれているのはそのため

### どのようにして絵文字になるのか

1. 絵文字のアイデアの企画書を書く
2. それを絵文字部会に提出し、部会では議論を重ねて検討する
3. フィードバックを受けて修正する
4. 納得のいくものができたらUnicodeの技術委員会に提出される
5. 年に1度、投票が行われ次の年の絵文字を通過させる
    - Apple、Google、Adobe、Facebookなどのすべての企業に送信されるので時間がかかる
6. 絵文字がデバイスに追加される！
    - ここまで1年半〜2年かかる

### 絵文字になるにはどのような点によって決まるのか

- 多くの需要があるかどうか
  - 非常に粗い測定方法の一つとしてGoogle検索したときに`5億件以上`の検索結果があるか
- 複数の使用方法や意味がある場合
  - 例えばナマケモノの絵文字は動物も意味するが、状態の比喩としても使用できる
- 視覚的に特徴的なもの
  - 絵文字は小さいので小さすぎても機能するもの
  - キムチは表現が難しいので実現しなかった

## 感想

講義の前半はWeek0〜Week9までの学習を振り返ってクイズ形式のテスト、後半戦は絵文字についての話

前半ではクイズの他にCS50の目的についての説明もあり、計算機的思考、思考プロセスを整理し、より論理的かつ几帳面に考えられるようにすること、エンジニアとして何かを作ることを求められたり、管理職として何かを作るべきだと判断したりした時はそれがどんな目的のためなのかよく考える。本当に「これをやるべきなのか」と他人に問いかけるべきということが言及されていた。

エンジニアとしてプロダクトを開発する上で、開発する機能の背景や目的を理解することはとても重要だと感じており、CS50で上記の事が言及されているのはとても良いと思った。

後半の絵文字の講義では絵文字は日本から始まったということで、日本の食べ物が多く含まれており、絵文字がどのようにして作られるのか、どのような点によって決まるのかなど、絵文字についての話は興味深かった