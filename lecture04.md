# 第4回目の課題

## VPCの作成

![VPCの作成](image/lecture04/VPC作成.png)

## EC2の作成

![EC2の作成](image/lecture04/EC2作成.png)

## RDSの作成

![RDSの作成](image/lecture04/RDS作成.png)

EC2にSSHクライアントで接続

![EC2に接続](image/lecture04/RDSに接続.png)

RDSに接続

![RDSに接続](image/lecture04/RDSに接続.png)

## 学んだこと

* EC2とRDSの作り方を間違えたりして何回も作り直してしまったので次は気をつける
osを間違えたり、パブリックIPアドレスを作らない設定して上手く接続できずにいた。
* RDSの接続も手こずった　MySQLのコマンドを理解していなかったりパスワードを入力しても接続出来ず、セキュリティーグループのインバウンドルールに設定を追加しても出来ず、最終的にRDSのパスワードをリセットしたら接続できた。
どれが有効的だったのかはわからなかった。