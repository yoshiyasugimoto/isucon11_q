# isucon11_q

## pprof-nodejs

1. ローカルにライブラリインストール

```
go install github.com/google/pprof@latest
```

2. 実行 ※サーバからローカルに`wall.pb.gz`(rsync)

```
cd webapp/nodejs
~/go/1.18.3/bin/pprof -http=: wall.pb.gz
```

## プロファイリング方法

- server[1-3]

```
cd webapp/nodejs
npm run build && npm run start
```

- bench

```
cd bench
./bench -all-addresses isucondition-[1-3].t.isucon.dev -target isucondition-[1-3].t.isucon.dev:443 -tls -jia-service-url http://bench.t.isucon.dev:8080
```

### 見方

peak を見ると実行するのにかかった時間が見れて良さげ
