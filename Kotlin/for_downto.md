# for文とdownTo
Kotlinでのfor文は次のように書く。
```kotlin
for (i in 0..5) {
    println(i)
}
```
0から5までループする。多言語でよくあるfor文は以下のように書き、5回ループすると捉えるが、上記の文では6回ループするため慣れる必要がある。
```java
for (int i; i < 5; i++) {
    println(i);
}
```
拡張for文も使える。
```Kotlin
for (i in array) {
    println(i)
}
```
以下のようにdownToを用いると、5から0へ逆へ進める事ができる。
```Kotlin
for (i in 5 downTo 0) {
    println(i)
}
```
しかし、つぎの書き方ではループは一度も行われない。IDEに __This ranges empty.__ と言われるので、for文では右の値から左の値を引いた結果がループ回数になっていると考えられる。
```Kotlin
for (i in 5..0) {
    println(i)
}
```
