# RaiseTech AWSコース

## 概要

- CRUD処理ができる簡単な[Railsアプリケーション](https://github.com/yuta-ushijima/raisetech-live8-sample-app)のインフラストラクチャを構成しました
- CI/CDツールのcircleciを使用して、AWSリソース構築から環境構築とデプロイを自動化しました
- 環境構築にはプロビジョニングツールのansibleを使用しました

#### 構成図
![構成図](image/lecture13/AWS.構成図.自動化処理図.drawio.png)

## 環境構築説明
### 概要

 ##### コードの詳細は[別リポジトリ](https://github.com/ReoNakamura/lecture13)に記載しています
1. Cloudformationを使用してEC2・RDS・S3を構築
2. Ansibleを使用してEC2にRailsアプリケーションの実行環境の自動構成
3. Serverspecを使用して条件が合致しているかサーバーが応答しているか確認
4. Circleciを使用して全て自動化
 
### 事前設定

- Circleciで環境変数の設定をしています
- 環境変数の方法は[lecture13.md](lecture13.md)を見てください
  - AWS-access-key
  - AWS-region
  - AWS-secret-key
  - fingerprint(事前に用意したキーペア)

- IAMでcircleciユーザーを作成して必要な権限を付与してアクセスキーを作成しました

### 学習記録
下の表に講座概要と提出課題の対応を示しています

|講座|概要|提出課題|備考|
| ----| ------------------------------------------------------------------| ------| -----|
|第1回| AWSアカウントの作成<br>IAMユーザーの作成<br>MFAの設定<br>Cloud9の作成|該当なし|Discord上に提出のため|
|第2回| GitHubのアカウント作成<br>Pull Requestの練習|[lecture02.md](lecture02.md)|Cloud9のターミナルで実施|
|第3回| Web アプリケーションについて<br>[サンプルアプリケーション(Rails)](https://github.com/yuta-ushijima/raisetech-live8-sample-app)のデプロイ|[lecture03.md](lecture03.md)|以降、ssh接続はmacのターミナルから実施|
|第4回| VPC,EC2,RDSの構築<br>EC2からRDSに接続の確認|[lecture04.md](lecture04.md)||
|第5回| EC2に手動でサンプルアプリケーションをデプロイ<br>データの保存先をS3に変更<br>ELB(ALB)で冗長化<br>構築した環境の構成図の作成|[lecture05.md](lecture05.md)||
|第6回| CloudTrailでの証跡、ロギング<br>CloudWatch,AmazonSNSで監視と通知<br>コスト管理<br>Cost Explorer<br>Billing|[lecture06.md](lecture06.md)||
|第7回| システムにセキュリティの基礎<br>AWSでセキュリテイィ対策| [lecture07.md](lecture07.md)||
|第8回| 第5回課題のライブコーディング(1)|該当なし||
|第9回| 第5回課題のライブコーディング(2)|該当なし||
|第10回| Cloudformationを使用してインフラ自動化(Infrastructure as Codeの実践)|[lecture10.md](lecture10.md)|SAAの資格取得|
|第11回| インフラのコード化を支援するツール<br>インフラのテスト<br>ServerSpec|[lecture11.md](lecture11.md)||
|第12回| CI/CDツールについて<br>CircleCIの導入<br>提供されたCircleCIの[サンプルコンフィグ](https://github.com/MasatoshiMizumoto/raisetech_documents/blob/main/aws/samples/circleci/config.yml)を実行|[lecture12.md](lecture12.md)||
|第13回| 構成管理ツール<br>Ansibleの導入<br>CircleCIとの併用| [lecture13.md](lecture13.md)|実施したコードの詳細は[こちら](https://github.com/ReoNakamura/lecture13)|
|第14回| 第13回課題のライブコーディング(1)|該当なし|README.mdに構成図と学習記録を追加|
|第15回| 第13回課題のライブコーディング(2)|該当なし||
|第16回| 現場へ出ていくにあたって|該当なし||
||||
