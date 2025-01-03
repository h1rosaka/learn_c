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