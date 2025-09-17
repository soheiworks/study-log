printfとの使い分け：printfに直接書く場合は、毎回固定された表示になる。

char変数を使う場合

①Yes / No 判定に使う
―　―　―　―　―　―　―　―　―　―　―　
\#include <stdio.h>

int main(void){

char c;

printf("続けますか？(y/n):");
scanf("%c", &c);

if ( c == 'y' || c == 'Y'){
    printf("はい、続けます。\n");}

else if ( c == 'n' || c == 'N'){
    printf("いいえ、終了します。\n");}

else {
    printf("yまたはnを入力してください\n");}

return 0;

}
―　―　―　―　―　―　―　―　―　―　―　
↑このコードでは、char に y, Y, n, N, それ以外の文字を代入して、代入された文字を判定する。
 条件分岐をさせるには変数を使う必要があり、文字を変数に入れるためにchar を使う。


②繰り返し処理で使う
―　―　―　―　―　―　―　―　―　―　―　
\#include<stdio.h>

int main(void){
    char c;

    for (c = 'A'; c <= 'Z'; c++){
        printf("%c",c);
    }

    printf("\n");

    return 0;
}
―　―　―　―　―　―　―　―　―　―　―　


③文字列から文字を抜き出して使う
―　―　―　―　―　―　―　―　―　―　―　
\#include <stdio.h>
int main (void){

    char str[] = "HELLO";
    int i;

    for (i = 0; str[i] != '\0'; i++){
        char c = str[i];
        printf("%c\n",c);
    }

    return 0;
}
―　―　―　―　―　―　―　―　―　―　―　


⭐char 型の変数は、1文字しか扱えないわけではない。
―　―　―　―　―　―　―　―　―　―　―　
\#include<stdio.h>
int main(void)
{
    //1文字だけのchar変数
    char c = 'A';
    printf("char変数 c の内容: %c\n", c);

    char str[] = "Hello";
    printf("char 配列 str の内容: %s\n", str);

    //配列の中身を1文字ずつ見る
    printf("str[0] = %c\n", str[0]);
    printf("str[1] = %c\n", str[1]);
    printf("str[2] = %c\n", str[2]);
    printf("str[3] = %c\n", str[3]);
    printf("str[4] = %c\n", str[4]);
    printf("str[5] = %d (終端文字 '\\0'\n", str[5]); //← \0(ヌル文字)を入れないと、いつまでもメモリを読みに行くので、関係ないメモリに入っている無関係な値を出力してしまう。
    return 0;
}

■↓実行結果
char変数 c の内容: A
char 配列 str の内容: Hello
str[0] = H
str[1] = e
str[2] = l
str[3] = l
str[4] = o
str[5] = 0 (終端文字 '\0'


⭐ただし、1文字ずつ順番を付けて格納しているため、条件分岐をするときはX番目の文字で比較、という使い方になる。

\#include <stdio.h>
int main(void){
    int number = 100 + 30;
    printf("%d\n", number);
    number = 100;
    printf("%d\n", number);

    char greeting[100] = "Hello world";
    printf("%s", greeting);

    return 0;
}

↑このコードのchar greetingには \n が無いが、”Hello World”　の最後の ” が来たところに、コンパイラが自動で\nを追加している。


