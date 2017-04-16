# lcutmisc

ここにあるパッケージの使い方を書いておきます．いまのところ日本語だけです．

各種動作条件等はそれぞれのマニュアルを参照してください．

## lcutrinko
大学院輪講の発表資料などに使用できるパッケージです．使い方などの詳細は以下のファイルを参照してください．

- `lcutrinko.sty`: 本体
- `lcutrinko-manual.tex`と`lcutrinko-manual.pdf`: マニュアル ここに使い方は書かれています．
- `lcutrinko-sample-ja.tex`と`lcutrinko-sample-ja.pdf`: 日本語での使用例
- `lcutrinko-sample-en.tex`と`lcutrinko-sample-en.pdf`: 英語での使用例

## lcutronbun
卒業論文などの表紙を書くためだけのパッケージです．あまり利用価値はないかもしれない．

### 使い方

#### 読み込み
プレアンブルで geometry を読み込んだ後に lcutronbun を読み込ます．内部で geometry パッケージの機能を使用しているので，geometry が先に読み込まれていないとエラーになります．

#### 設定項目
卒業論文フォーマット用にいくつか命令を定義しています．
- \title{} 題目
- \date{} 提出日
- \author{} 氏名
- \department{} 所属学科
- \idnumber{} 学籍番号
- \mainsupervisor{} 筆頭指導教員（内部で改行は禁止）
- \subsupervisor{} （オプション） その他の指導教員（同様に内部での改行禁止）
- \ronbun{} （オプション） 論文種類を指定．デフォルトでは「卒業論文」
- \supervisorfield{} （オプション） デフォルトで「指導教員」という欄を変更する

以上の命令で諸々設定のうえ，本文中で \maketitle すると表紙が描画されます．

#### 注意
\mainsupervisor と \subsupervisor を両方使い複数の指導教員の氏名を入れると，表紙の体裁は文字数の多い方に合わせられます．事務室のテンプレートのごとく職階をそろえたい場合は，自ら全角空白や \hspace 命令を使用して揃えてください．

### バージョン
- Ver 1.0 事務室掲示の学科卒業論文の体裁に近くなるようにつくる
- Ver 1.1 2017-02-01 間違って（というか理解不足で）@maketitleを上書きしていたのをmaketitleにする（これでjsarticle系統意外でも使えるようになる）
