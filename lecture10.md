# 第10回課題
## cloudformationを利用して環境構築をコード化する

### 第５回と同じ環境をテンプレートで構築
- スタック  
VPC.YAML  
EC2-RDS.YAML  
の二分割で構成
- テンプレートのコードはlecture10-imageのCF-Templateファイルに保存

## 構築した環境

- VPC

![](lecture10-image/TestVPC.png)
- IGW
![](lecture10-image/TestIGW.png)
- SecurityGroup
![](lecture10-image/SecurityGroup(EC2,RDS).png)
- ALB
![](lecture10-image/ロードバランサー.png)
- EC2
![](lecture10-image/EC2.png)
- EC2接続
![](lecture10-image/EC2接続.png)
- RDS
![](lecture10-image/RDS.png)
- RDS接続
![](lecture10-image/RDS接続.png)
