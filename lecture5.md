# 第５回  
## 講義内容  
* EC２にアプリケーションのデプロイ  
* ELB 経由で EC2 へ接続(冗長化・負荷分散)  
* アプリケーションのデータ保存先をS3に変更  
* S3　の別の役割  
* インフラ構成図を書く  
# 課題内容  
## EC2上に組み込みサーバーを利用しデプロイをする。  
* 必要なソフトウェアのインストールをし環境構築実施  
  * ruby・node・yum・git・MySQL・Swapの設定  課題内容  
  ![puma](IMG/EC2.rails.png)  
## WEBｻｰﾊﾞｰとAPｻｰﾊﾞｰを分けた状態でデプロイをする  
* Nginx・unicornのインストール  
  * pathや挙動を確認しながらconfigの設定  
　![server](IMG/unicorn‗nginx.png)   
## ELB(ALBの追加)  
* ターゲットグループの作成・セキュリティグループの作成 ・インスタンスのセキュリティグループ追加  
　![ELB](IMG/ELB.png)  
* ALBでのデプロイ  
　![ALB](IMG/alb.png)  
## S3の作成
* IAMロールの追加・保存先をS3に変更 
　![S3](IMG/lecture5/s3.png)  
## S3を反映しデプロイ メロンを追加 
  ![S3](IMG/S3.on.png)  
 