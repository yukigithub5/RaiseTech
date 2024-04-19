# *rubyインストール*
* Ruby（ルビー）は、日本で開発されたオブジェクト指向スクリプト言語  
## 本体のインストール
``` $ git clone https://github.com/sstephenson/rbenv.git ~/.rbenv ```  
## pathを通す  
``` $ echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.bash_profile ```  
``` $ echo 'eval "$(rbenv init -)"' >> ~/.bash_profile ```  
``` $ source ~/.bash_profile ```  
## ruby‐buildのインストール  
``` $ git clone https://github.com/sstephenson/ruby-build.git ~/.rbenv/plugins/ruby-build  ```  
## インストールスクリプトの実行  
``` $ cd ~/.rbenv/plugins/ruby-build ```  
``` $ sudo ./install.sh ```
## インストール
``` $ sudo yum install -y openssl-devel readline-devel zlib-devel ```  
``` $ rbenv install 3.1.2 ```  

# *nodeのインストール*  
* ブラウザ上という制限された環境でしか動けなかったJavaScriptを、PythonやRubyのようにパソコン上で動かせるようにしてくれるのが「Node.js」 
## yumコマンドでシステムのアップデート  
``` $ sudo yum update ```  
## g＋＋コンパイラのインストール    
``` $ sudo yum -y install gcc-c++ ```  
## nvmのインストール  
* 複数のNode.jsのバージョンを管理することができるようになるbashスクリプト  
``` $ git clone https://github.com/creationix/nvm.git ~/.nvm ```  
## path  
``` $ source ~/.nvm/nvm.sh ```  
``` $ vi .bash_profile ```  
* Vim にて.bash‗profile編集  
``` # nvm ```  
``` if [[ -s ~/.nvm/nvm.sh ]] ; then ```  
```        source ~/.nvm/nvm.sh ; ```  
 ```fi ```  
 ## インストール可能なバージョン一覧  
``` $ nvm ls-remote ```  
Node.jsのインストール  
``` $ nvm install 5.0.0 ```  
使用するversion指定  
``` $ nvm use v17.9.1 ``` 
