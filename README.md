# LSTM使って日経平均の予測をしよう

## 記事
https://cpptake.com/archives/525


## やりたい事
<br>時系列データの分析に適したアルゴリズム、LSTMを利用して日経平均の予測モデルを作成した。
<br>LSTMもモデルを1モデル作成したのち、2つの方法で検証を行った。

1. テストデータを検証データに分割し、検証データでの予測結果を計算
2. テストデータを与えない状態で、未来の株価を予測


結果、
1. の場合はval_lossは収束したが、予測結果は過去の株価の値を後追いするようなラグモデルになり
2. は株価が収束し、予測結果と実測値の乖離がすさまじくなった。



## バージョン
Keras：2.3.1
pandas:1.2.3
numpy:1.19.2


### 参考文献
* https://qiita.com/kazukiii/items/df809d6cd5d7d1f57be3
* https://www.codexa.net/keras-lstm-cryptos-forecast/
* http://tekenuko.hatenablog.com/entry/2017/07/25/005348


### データセット参照先
* http://k-db.com/

