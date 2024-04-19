## configfaileに〈200b〉がはいっていた。
nginx: [emerg] unknown directive "​" in /etc/nginx/nginx.conf:43
nginx: configuration file /etc/nginx/nginx.conf test faile  
## blockd:host  
config/environments/development.rb に
Rails.application.configure do
    config.hosts << "unicorn"
end　を追加  
## master failed to start, check stderr log for details　unicorn起動後  
development.rb にendが多かった  
## リバースプロキシの設定  
* vi nginx.confに追加  
```  location @unicorn { ```
       　   proxy_pass http://unicorn; 
       ```  proxy_set_header Host $http_host; ```
       ```　proxy_set_header X-Forwarded-Proto $scheme; ```
``` proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;  ```
## ポート3000　→　80　に変更  
``` etc/nginx/nginx.conf ```  
## DNSをホストに追加 *上記ディレクトリ