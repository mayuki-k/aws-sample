## ビルド

```
docker build -t test .
```

## コンテナ作成

```
docker run -itd --name yuki test /bin/sh
```

## dockerの中に入る

```
docker exec -it yuki /bin/bash
```