# Script Wiki

Link : https://scratch.mit.edu/projects/1170052574/
<br><br><br><br><br>
## クイックリンク
* [構文](https://github.com/hiracmc/scriptwiki/blob/main/README.md#code)
* [デフォルトの変数一覧](https://github.com/hiracmc/scriptwiki/blob/main/README.md#%E5%91%BC%E3%81%B3%E5%87%BA%E3%81%99%E3%81%93%E3%81%A8%E3%81%AE%E3%81%A7%E3%81%8D%E3%82%8B%E5%A4%89%E6%95%B0%E4%B8%80%E8%A6%A7)
* [条件一覧](https://github.com/hiracmc/scriptwiki/blob/main/README.md#%E6%9D%A1%E4%BB%B6%E4%B8%80%E8%A6%A7)
* [サンプルコード](https://github.com/hiracmc/scriptwiki/blob/main/README.md#%E3%82%B5%E3%83%B3%E3%83%97%E3%83%AB%E3%82%B3%E3%83%BC%E3%83%89)
<br><br><br><br><br>
## code

`太字のテキストの説明`

`text : テキスト。変数を呼び出すことができる`

`size : 大きさ。`

`x,y : 座標。`

`color : カラーコード。#は不要。`

`num : 数字。変数を使用できる`

`code : コード`

`name : 任意の名前`


| 構文 | 説明 |
|:-----------|:------------|
| p(__text__) | コンソールにテキストを出力 |
| tx(__text__,__size__,__x__,__y__,__color__) | テキストを表示する。英数字のみ対応 |
| v __name__ = __text__; | 変数を作成 or 変更する |
| bgc(__color__) | 背景の色を変更します |
| rep(__num__){<br>__code__<br>} | 繰り返し |
| loop{<br>__code__<br>} | ループ |
| timer reset | タイマーをリセット |
| px(__x__,__y__,__x2__,__y2__,__枠の太さ__,__color__) | 四角形を表示する |
| ask(__text__) | 回答を要求する。このコードを実行した時点で&answerは空になる |
| if(){<br>__code__<br>}| ()内の条件を満たした場合のみ実行する<br>条件一覧は[下](https://github.com/hiracmc/scriptwiki/blob/main/README.md#%E6%9D%A1%E4%BB%B6%E4%B8%80%E8%A6%A7)へ |

<br><br><br><br><br>
### 呼び出すことのできる変数一覧
| 呼び出し方 | なにか |
|:-----------|:------------|
| &timer | タイマーを取得 |
| &sin(__num__) | sinを取得。$timerも使用できる。numが&timerの場合は、 $sin(__num__,__num__) に構文が変化する。2個目のnumには、タイマーを何倍にするかを入力する |
| &cos(__num__) | cosを取得。$timerも使用できる。numが&timerの場合は、 $cos(__num__,__num__) に構文が変化する。2個目のnumには、タイマーを何倍にするかを入力する |
| &rdn(__num__,__num__) | ランダムな数を生成する |
| &clock(__name__)| 時間を取得 <br> Second : s <br> Minute : m <br> Hour : h <br> Day : d <br> Week : w <br> Month : mo <br> Year : y |
| &answer | 回答を取得 |
| &length(__text__) | 長さを取得 |
| @__name__ | 自分で作った変数を取得 |


<br><br><br><br><br>
### 条件一覧
| 書き方 | 説明 |
|:-----------|:------------|
| 条件の書き方 | if {a = a,touch()} { <br>条件の間には空白は入れない。また、条件が2つ以上の時は,で繋げる|
|  |  |
| touch(__x__,__y__,__x2__,__y2__) | マウスが指定された座標内に存在するか調べる |
| __text__ = __text__ | 2つの要素が一致しているか調べる |



<br><br><br><br><br><br><br><br><br><br>

### サンプルコード

・動くテキスト
`
loop{|bgc(00ffff);|v a = &sin(&timer,300);|v b = &cos(&timer,300);|tx(text,50,@a,@b,000000)|}|
`

・すべての問いに答えるAI
`

`
