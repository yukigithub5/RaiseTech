# 第7回  
## 講義内容  
* システムにおけるセキュリティの基礎  
* セキュリティ対策計画の主体は誰が適切？  
* AWSでのセキュリティ対策(脆弱性)  
* AWSでのセキュリティ対策(認証情報の流出)  
* AWSでのセキュリティ対策(人為的な過負荷)  
* AWSでのセキュリティ対策(その他知っておくべきサービス)  
## 講義の感想  
 ITパスポートの資格をとる際に勉強はしていたが、正直今でもピンとこない。  
 その為、どういう対策をとればいいのか浮かんでこない。  
 ただ、今後は絶対に関わっていく事になるので勉強していこうと思った。  
## 自分の制作環境の脆弱性  
* EC2のセキュリティグループでのインバウンドルールにport80を解放しているが、MyIPのみ許可しているので問題無いと判断した。  
ただし、認証情報の流出等の危険がある。現にキャプチャした画像のAWSアカウントの消し忘れがあった。今後課題に対してもそういった観点で抜け漏れをさがしていこうと思う。