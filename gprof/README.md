# gprof
gprofはglibcに付属しているプロファイラ。手軽使える。


docker イメージのビルド.
```
$ docker build -t gprof-test .
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
