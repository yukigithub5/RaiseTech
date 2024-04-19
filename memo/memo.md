# *yarn のインストール*
## yarnとは
JavaScriptのパッケージマネージャ  
2016年にFaceBookが公開した
npmと互換性がある = 同じpackage.jsonが使える  
yarnのメリット
npmよりインストールが速いく
約半分になる場合もあるそう
npmより厳密にモジュールのバージョンを固定できる
yarn.lockファイルで、各パッケージのインストールバージョンを固定できる。  
npmと一緒に使える
npmと同じのpackage.jsonが使えるため、同一プロジェクトでnpm or yarnで固定しなくて良い。

### installコマンド  
``` $ sudo npm install -g yarn ```  
### package.jsonの生成  
パッケージを一括管理できるpackage.json  
``` $ yarn init ```  
yarn add package-nameは、package.jsonに別の指定がされていなければ、npmレジストリからパッケージをインストールします。
yarn add file:/path/to/local/folderは、ローカルのファイルシステム上のパッケージをインストールします。これはレジストリに公開されていない、あなた自身のパッケージをテストするのに便利です。
yarn add file:/path/to/local/tarball.tgzは、パッケージの公開前に共有することができるgzip圧縮されたtarアーカイブから、パッケージをインストールします。
yarn add <git remote url>はリモートのgitリポジトリからパッケージをインストールします。
yarn add <git remote url>#<branch/commit/tag>は、指定されたリモートgitリポジトリのgitブランチ、gitコミット、またはgitタグのからパッケージをインストールします。
yarn add https://my-project.org/package.tgzは、リモートのgzip圧縮されたtarアーカイブからパッケージをインストールします。
### yarnでパッケージをインストール  
package.jsonに記載されたモジュールをインストールする  
``` $ yarn ``` 6500 4490