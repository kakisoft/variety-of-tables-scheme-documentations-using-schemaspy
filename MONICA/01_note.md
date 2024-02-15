## docker hub
https://hub.docker.com/_/monica/  

docker-compose.yml は、公式記載の内容から、少し修正しています。  

```yaml
  ports:
    - "3306:3306"
```

## 起動・終了
```
docker-compose up -d
docker-compose down
```

## 終了時にコンテナを削除
```
docker-compose down --rmi all
docker-compose down --rmi all --volumes
```

## テーブル定義作成
```
docker-compose -f docker-compose-schemaspy.yml up
```

## テーブル作成用のコンテナを終了・削除
```
docker-compose -f docker-compose-schemaspy.yml down
docker-compose -f docker-compose-schemaspy.yml down --rmi all --volumes
```

____________________________________________________________________________________

