# Nginxとは，  
* NGINXはWebサーバーソフトでWebサーバーとは、ユーザーからのリクエストを受けて処理を実行し、ユーザーにレスポンスを返すためのコンピューターのこと  
# unicornとは、 
* UnicornとはRackアプリケーション用のWebサーバーで、Unicornは送信されてきた多数のリクエストを捌き、分散してアプリケーションに伝達するという機能を持つ。リクエストをアプリケーションへ伝達するとアプリケーションからレスポンスが戻ってくるまで待機し、最終的にリクエストに対するレスポンスをクライアントに返す。
## Nginxリポジトリ作成 ない状態だとインストールできない。  
``` $ sudo yum install http://nginx.org/packages/centos/7/noarch/RPMS/nginx-release-centos-7-0.el7.ngx.noarch.rpm -y ```  
## nginx インストール  
``` $ sudo yum install nginx -y ```  
## 接続状況確認（Active: inactive (dead)）確認
``` $ sudo systemctl status nginx.service ```  
## 接続開始  
``` $ sudo systemctl start nginx.service ```  
## 接続状況確認（Active: active (running)）確認
``` $ sudo systemctl status nginx.service ``` 
## 停止コマンド  
``` $ sudo systemctl stop nginx.service ```  
## unicornとRailsアプリケーションの接続設定  
``` $ sudo vi /etc/nginx/nginx.conf ```
* https://qiita.com/Takao_/items/b18234b8db4cda97a113　参照  
## railsアプリとRDSの接続設定  
``` $ vi config/database.yml ```  
* 上記URL  参照  
``` $ vi Gemfile ```  
``` gem "unicorn"  #追加 ```  
``` $ bundle install --path vendor/bundle ```  
## unicornの設定  develoment
``` $ sudo mkdir -p config/unicorn ```  
``` $ sudo vi config/unicorn/development.rb ```  
* 上記URL  参照  
## ログの作成  
``` $ touch log/unicorn.stderr.log ```  
``` $ touch log/unicorn.stdout.log ```  
``` $ mkdir -p tmp/pids ```  
``` $ mkdir -p tmp/sockets ```  
## unicornの起動  
``` $ bundle exec unicorn_rails -E development -c config/unicorn/development.rb -D ```  
## プロセスファイルでの起動確認  
``` $ ps -ef | grep unicorn | grep -v grep ```  
## nginxの起動  
``` $ sudo systemctl start nginx.service ```   
``` $ ps aux | grep nginx ```  
## nginx.confの設定  

## nginx保存先
user/etc/nginx
