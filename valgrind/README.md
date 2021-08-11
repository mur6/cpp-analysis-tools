# Valgrind
メモリデバッグや、メモリリークの検出、スレッドエラーの検出、プロファイリングなどを行うための、仮想機械を利用したツール.

## 環境構築
下記のコマンドにて、docker上のテスト環境をビルドする。
```
$ docker build -t valgrind-test .
```

## サンプルプログラムのビルド
サンプルプログラムのビルドと、動作確認。
```
# g++ main.cpp -pg -o main
# ./main
Hello, world.
```



## 参考サイト
- [プロファイラの比較（＋簡単な使い方） - Qiita](https://qiita.com/awrznc/items/161b55c29e6596431ca4#gprof)
