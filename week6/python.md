# [Week6 Python](https://cs50.jp/x/2022/week6/)

## Python

[docs.python.org](https://www.python.org/)

## C言語とPythonの比較

### コードが簡潔

- C言語と比較して簡潔なコードが書ける構文が用意されている

```python
answer = get_string("What's your name?　")
print(f"hello, {answer}")
```

### 型

- 型宣言をしなくても文脈で型を判断してくれる
- 関数の戻り値と引数や変数の型を指定しない
- Python 3.5（2015年9月リリース）で型ヒントが導入された

```c
// C
int counter = 0;
```

```python
# Python
counter = 0
```

### 配列

- C言語ではサイズが固定されているが、Pythonでは空の配列を作成できる
- `+`を使って2つのリストを結合できる

```python
# Python
scores = []
for i in range(3):
  score = get_int("Score: ")
  scores += [score]
average = sum(scores) / len(scores)
print(f"Average: {average}")
```

### 条件分岐・ループ

- Pythonではインデントが重要
- 一貫性がある限りダブルクウォート、シングルクウォートを使うことができる

```c
// C
if (x < y) {
  printf("x is less than y\n");
}
```

```python
# Python
if x < y:
  print("x is less than y")
```

```python
# Python
def meow(n):
  for i in range(n):
    print("meow")
```

### 実行

- コンパイラの実行が不要で、すぐにコードの実行に移れる
- C言語ではmain関数が必須であったがPythonでは不要

```
python hello.py
```

## exceptions（例外処理）

```python
try:
  x = int(input("x: "))
except ValueError:
  print("That is not an int!")
  exit()
try:
  y = int(input("y: "))
except ValueError:
  print("That is not an int!")
  exit()
print(x + y)
```

## 感想

過去数週間学んだC言語からPythonへ移行し、C言語とPythonを比較した講義

動的型付け言語ではJSが書けるので、Pythonの文法は理解しやすかった

講義の中でC言語とPythonでスペルチェッカーを実装したところ、C言語で実行した場合は約3秒、Pythonで実行した場合は約11秒かかった。実行時間だけ見ればC言語や優勢だが、Pythonであればコードの実装に費やす時間も少なく、コンパイルも不要だし、C言語ではメモリ管理とコードの実装が大変であり、バグも発生しやすいことからプログラマにとってはPythonの方が生産性が高いなと感じた。

新しい言語を使うポイントは他の人が実現してくれた抽象化を活用すること、ということも語られており、C言語で大変だった実装もPythonではライブラリなどを用いて簡潔に実装できていた。

また、新しい言語を学ぶ際のゴールは網羅的に学ぶことではなく、新しい言語を使って遊んだり、学んだりすることが目的であるということも語られていたのも印象的であった。