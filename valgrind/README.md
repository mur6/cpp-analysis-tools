# Valgrind
メモリデバッグや、メモリリークの検出、スレッドエラーの検出、プロファイリングなどを行うための、仮想機械を利用したツール.

## 環境構築とコンテナの起動
下記のコマンドにて、docker上のテスト環境をビルドする。
```
docker build -t valgrind-test .
```

下記のコマンドにて、コンテナを起動して下さい。
```
docker run -it --rm -v "$PWD":/src --name valgrind-env valgrind-test
```

## プログラムのビルドと実行
コンテナ内にて、プログラムのビルド及びvalgrindによるプロファイリングを実行して下さい。
```
root@ca9ac5980dcc:/# cd /src
root@ca9ac5980dcc:/src# g++ -std=c++11 main.cpp -o main
root@ca9ac5980dcc:/src# valgrind --tool=callgrind ./main
root@ca9ac5980dcc:/src# exit
```


## 参考サイト
- [プロファイラの比較（＋簡単な使い方） - Qiita](https://qiita.com/awrznc/items/161b55c29e6596431ca4#gprof)
