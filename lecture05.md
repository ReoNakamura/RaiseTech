# 第5回課題
* 組み込みサーバーで起動
![puma駆動](image/lecture05/puma起動.png)
![puma起動確認](/image/lecture05/puma起動確認.png)
* nginxとunicornで分けてデプロイ
![nginxとunicorn起動](image/lecture05/nginxとunicornの起動.png)
![接続確認](image/lecture05/nginxの接続確認.png)

![デプロイ確認](image/lecture05/nginxとunicornでデプロイ.png)

# ALBの導入
* ALBを経由してサンプルアプリのデプロイ
![ALB経由](image/lecture05/ALB経由でデプロイ.png)
# アプリのデータ保存先をS3に変更
* データの保存先をS3した
![S3にデータを保存](image/lecture05/S3にデータを保存１.png)
![S3にデータを保存](image/lecture05/S3にデータを保存2.png)
![S3にでーたを保存](image/lecture05/S3にデータを保存３.png)

# インフラ構成図
![構成図](image/lecture05/AWS構成図.drawio.png)

## 学んだこと
課題を終えるのにすごく時間がかかった。  
EC2の作り直しやヘルスチェックの問題など、色々なとことでつまづいた。  
環境が壊れた時のために手順書を予め作っておくともしもの時にすぐに元に戻せるのでこれからは何をしたかメモを残すようにする。  
S3に保存先を変えるのも難しくしていただけで分かるとすんなり出来た。本番環境でやろうとしていたけど本番環境にするだけでやることが多くて進めることが出来なかった。