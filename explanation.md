# SchemaSpy

## SchemaSpy とは？
ER図を自動生成するツール。  

例えば、こちらのサンプルをご参照ください。  
[MONICA](https://kakisoft.github.io/variety-of-tables-scheme-documentations-using-schemaspy/MONICA/db_docs/index.html)


## 何が凄いの？

### フィルタリングができる
「Search」にキーワードを入れて、条件の絞り込みができる。  
検索した内容は、リアルタイムに反映される。  

### リレーション数を限定して表示する事ができる
ER図作成ツールでありがちな事：全テーブルと全テーブルのリレーションが出力され、ごちゃごちゃし過ぎて何が書いてあるのか分からず、結局活用されない。  

例）[こんな感じ](https://kakisoft.github.io/variety-of-tables-scheme-documentations-using-schemaspy/MONICA/db_docs/relationships.html)  

SchemaSpy は、テーブルを指定すると、リレーション先の階層の数を指定して表示できる。  

例）[こんな感じ](https://kakisoft.github.io/variety-of-tables-scheme-documentations-using-schemaspy/MONICA/db_docs/tables/documents.html)  

情報過多に陥らず、現在の開発スコープに絞って調べる事ができる。  

### dockerコンテナで実行できる
公式サイトからコンテナが配布されている。  

以下のように、プロダクトと切り離した docker-compose を作成し、プロダクトのER図を作成する事ができる。  

[schemaspyを使用したdocker-composeファイルの例](MONICA/docker-compose-schemaspy.yml)

    [aaa](https://github.com/kakisoft/variety-of-tables-scheme-documentations-using-schemaspy/blob/main/MONICA/docker-compose-schemaspy.yml)


## あまり活躍出来ない場面
RDB上で外部キーを指定していない場合、リレーションが見えず、全て独立したテーブルと見なされる。  
（別に SchemaSpy に限った事ではありませんが。）

例）[Redmine](https://kakisoft.github.io/variety-of-tables-scheme-documentations-using-schemaspy/Redmine/db_docs/index.html)


