# [Week5 Data Structures](https://cs50.jp/x/2022/week5/)

## linked lists（連結リスト）

- 配列をメモリに保存するときに隣のメモリが空いていない場合のソリューション
- 連結リストでは配列の時とは違い、コンピュータのメモリをコントロールすることができる
- `malloc`にメモリを要求すると、`malloc`は渡したメモリのアドレスを有効な値として記録しておく
- 連結リストを使えば、連続したメモリの塊を大量に増やす必要がないので、より多くのメモリを使えるようになる

## NODE

- 情報をカプセル化したデータ構造がある場合はNODEと総称する
- データを保存するための一般的な用語

## binary search trees（二分探索木）

- 二分探索木は左の子ノードは親ノードよりも小さく、右の子ノードは親ノードよりも大きい
- データを追加するときにデータをソートされた状態で保存することができる

```c
typedef struct node {
	int number;
	struct node *left;
	struct node *right;
} node;
```

## hash tables

- キーと値を関連付けることができる
- JSで言うところのオブジェクトやJsonのようなもの

## tries

- 巨大なデータセットであっても一定時間で検索が可能なツリーのこと

## abstract data structures

### FIFO

- First In First Out

###  LIFO

- Last In First Out
- 古いデータほど、長く残るデータ格納方式

## 感想

C言語を学ぶのは今回のweek5までとなり、今回は一般的にデータ構造と呼ばれるものに焦点を当てた講義であった。

連結リストに関しては、配列のように連続したメモリの塊を大量に増やす必要がないので、より多くのメモリを使えるようになるという点が印象的で、こういったことも高水準言語では自動で行われているんだなと理解した。

Week0〜Week5ではコンピュータサイエンスの基礎を学ぶとともに、最近の高水準言語では少ないコードでより多くのことができるようになるが、その裏側にはC言語のような低水準言語の理解をする必要があるんだよということを学習できた。