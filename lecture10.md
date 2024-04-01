# 第10回課題
## cloudformationを利用して環境構築をコード化する

### 第５回と同じ環境をテンプレートで構築
- スタック  
VPC.YAML  
EC2-RDS.YAML  
の二分割で構成
- テンプレートのコードをimage/lecture10/のCF-Templateファイルに保存

## 構築した環境

- VPC

![](image/lecture10/TestVPC.png)
- IGW
![](image/lecture10//TestIGW.png)
- SecurityGroup
![](image/lecture10//SecurityGroup(EC2,RDS).png)
- ALB
![](image/lecture10//ロードバランサー.png)
- EC2
![](image/lecture10//EC2.png)
- EC2接続
![](image/lecture10//EC2接続.png)
- RDS
![](image/lecture10//RDS.png)
- RDS接続
![](image/lecture10//RDS接続.png)
