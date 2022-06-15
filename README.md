# isucon11_q

## pprof-nodejs

1. ローカルにライブラリインストール

```
go install github.com/google/pprof@latest
```

2. 実行 ※サーバからローカルに`wall.pb.gz`(rsync)

```
~/go/1.18.3/bin/pprof -http=: wall.pb.gz
```

### 見方

peak を見ると実行するのにかかった時間が見れて良さげ
