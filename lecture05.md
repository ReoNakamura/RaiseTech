# 第5回課題
* 組み込みサーバーで起動
![puma駆動](lecture05/puma%E8%B5%B7%E5%8B%95.png)
![puma起動確認](lecture05/puma%E8%B5%B7%E5%8B%95%E7%A2%BA%E8%AA%8D.png)
* nginxとunicornで分けてデプロイ
![nginxとunicorn起動](lecture05/nginx%E3%81%A8unicorn%E3%81%AE%E8%B5%B7%E5%8B%95.png)
![接続確認](lecture05/nginx%E3%81%AE%E6%8E%A5%E7%B6%9A%E7%A2%BA%E8%AA%8D.png)

![デプロイ確認](lecture05/nginx%E3%81%A8unicorn%E3%81%A7%E3%83%87%E3%83%97%E3%83%AD%E3%82%A4.png)

# ALBの導入
* ALBを経由してサンプルアプリのデプロイ
![ALB経由](lecture05/ALB%E7%B5%8C%E7%94%B1%E3%81%A7%E3%83%87%E3%83%97%E3%83%AD%E3%82%A4.png)
# アプリのデータ保存先をS3に変更
* データの保存先をS3した
![S3にデータを保存](lecture05/S3%E3%81%AB%E3%83%87%E3%83%BC%E3%82%BF%E3%82%92%E4%BF%9D%E5%AD%98%EF%BC%91.png)
![S3にデータを保存](lecture05/S3%E3%81%AB%E3%83%87%E3%83%BC%E3%82%BF%E3%82%92%E4%BF%9D%E5%AD%982.png)
![S3にでーたを保存](lecture05/S3%E3%81%AB%E3%83%87%E3%83%BC%E3%82%BF%E3%82%92%E4%BF%9D%E5%AD%98%EF%BC%93.png)

# インフラ構成図
![構成図](<lecture05/AWS 構成図.png>)

## 学んだこと
課題を終えるのにすごく時間がかかった。  
EC2の作り直しやヘルスチェックの問題など、色々なとことでつまづいた。  
環境が壊れた時のために手順書を予め作っておくともしもの時にすぐに元に戻せるのでこれからは何をしたかメモを残すようにする。  
S3に保存先を変えるのも難しくしていただけで分かるとすんなり出来た。本番環境でやろうとしていたけど本番環境にするだけでやることが多くて進めることが出来なかった。