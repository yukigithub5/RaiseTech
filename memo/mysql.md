# MySQLのインストール  
* Oracleが開発してサポートするオープンソースのSQLリレーショナルデータベース管理システム  
linux2にはMariaDBというMySQL互換のDBサーバーがインストールされている為削除しインストールする
``` $ curl -fsSL https://raw.githubusercontent.com/MasatoshiMizumoto/raisetech_documents/main/aws/scripts/mysql_amazon_linux_2.sh | sh ```  
## ログインコマンド  
``` $ mysql -u admin -p -h create1.c72s66a067yo.ap-northeast-1.rds.amazonaws.com ```  
``` Passwd :Nb19900514 ```
## データベース表示  
``` SHOW DATABASES; ```  
## データベース作成  
``` CREATE DATABASE raisetech_live8_sample_app_production ``` 
## 使用するデータベース選択  
``` USE ```  
## テーブルの作成
``` CREATE TABLECREATE TABLE users (id INT AUTO_INCREMENT, name TEXT, PRIMARY KEY (id)) DEFAULT CHARSET=utf8; ```  
users：作成するテーブルの名前
id：idというカラム名
INT：idカラムのデータ型が「整数」という意味。INTは英語のIntegerの略
AUTO_INCREMENT：idの数字を連続した値にすることが可能。例えば、id= 1, id= 2, id =3….という感じです。
name：nameというカラム名
TEXT ：nemeカラムのデータ型が「文字」という意味。
PRIMARY KEY (id) ：重複したidが生成されないようになります。  
例えばid=1,id=2が存在する場合、新しく生成されるidは1と2以外の数字となる  
## テーブルの表示  
``` SHOW tables; ```  
## DESCRIBEで作成したテーブルの中身を確認する  
DESCRIBE users;  
## DATABASEの削除  
``` DROP DATABASE rasetech_live8_sample_app_production; ```    
## データベースのデータを取得する  fruitsを表示させる
``` select * from fruits; ```  
mysql> select * from fruits;
+----+-----------+------------+----------------------------+----------------------------+
| id | name      | row_order  | created_at                 | updated_at                 |
+----+-----------+------------+----------------------------+----------------------------+
|  1 | apple     |          0 | 2024-01-23 13:24:35.303046 | 2024-01-29 05:59:51.177270 |
|  5 | いちご    | 2013265920 | 2024-01-30 09:24:03.444984 | 2024-01-30 09:24:03.468841 |
|  6 | ぶどう    | 2080374784 | 2024-01-30 09:56:03.759462 | 2024-01-30 10:40:40.156362 |
|  8 | すいか    | 2130706432 | 2024-01-30 10:31:01.812923 | 2024-01-30 10:31:01.839777 |
|  9 | バナナ    | 2139095040 | 2024-01-30 12:52:50.133482 | 2024-01-31 15:32:38.392478 |
+----+-----------+------------+----------------------------+----------------------------+
5 rows in set (0.00 sec)
