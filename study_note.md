なぜ、a.outでは実行できないのか?(./a.outにする必要があるのか)

    UNIX（Linux）は、DOS（Windowsのコマンドプロンプト）とは違い、カレントディレクトリにはPATHが通っていないのが普通です。したがって、a.outを実行するには、カレントディレクトリ上にあるファイルであることを明示するため、頭に./を付けて./a.outとコマンド入力する必要があるのです。
    https://gihyo.jp/dev/serial/01/c-programming-introduction/0004


「# include <stdio.h>　」は何か
    ヘッダファイルを読み込む処理
    ヘッダファイル：複数のプログラムで使う処理をヘッダファイルとして別に書き出す。(多分pythonのimport的な)
    stdio.hは standard io で、入出力を行うためのヘッダーファイル。gccによって提供されている。


```c


int main(){
    int a; // intの大きさでaという領域(メモリ)を確保してください
        //ちなみにintは4バイト

    a = 10;

    return 0;

}

```
![alt text](image.png)



a.outのaは何？
    アセンブラ　アウトプットのa.
    「gcc -o ./a.outの代わりの名前 ファイル名.c」で自由に保存する時の名前変えられる


C 言語のプログラムでは、どうして色々なデータ型を使い分けなければならないのでしょうか。int 型など使わずに、全てを double 型にできれば簡単です。

    プログラムを高速に実行するためです。普通のコンピュータは、例えば整数と小数で異なる演算回路（ハードウェア）を使いますが、整数用の回路の方が高速です。ですから、値の範囲が整数なら int 型を使った方がよいのです。そのぐらい、コンピュータが自動的に判別してくれればよさそうなものですが、少なくとも C 言語ではそのようなことはしてくれません。

    https://tcs.c.titech.ac.jp/csbook/c_lang/chap2.html



   関数名の前に書いてある型は、関数の戻り値の型。main 関数にも return 文を書くが、その戻り値は通常利用されない。この場合、 一般的に値が 0 の場合には実行が成功したことを、それ以外の値の場合は失敗したことを表すのが慣例。
   https://tcs.c.titech.ac.jp/csbook/c_lang/chap3.html



Cの配列を扱う時、宣言時の大きさを越えたインデックスを用いても、コンパイルエラーとはならず、また、プログラムがどう動作するか全く予測できない。
https://tcs.c.titech.ac.jp/csbook/c_lang/chap6.html

