Elastic Container Service

# コマンド

## 変数設定

```
aws configure --profile ecr
```

## ログインコマンドを取得

```
aws ecr get-login --region ap-northeast-1 --profile ecr --no-include-email
```

- ↑を打つと、docker loginのコマンドが返ってくるのでそのまま打つ

## buildを行う

- IMAGE_NAMEはECRのレポジトリと同じ名前

```
docker build -t {IMAGE_NAME} .
```

## タグの設定

```
docker tag {IMAGE_NAME}:latest {ECR_URL}:latest
```

## push

```
docker push {ECR_URL}:latest
```