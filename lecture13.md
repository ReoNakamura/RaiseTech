# 13回課題

##  CircleCIにServerSpecとAnsibleの処理を追加する

<details><summary>デプロイ自動化構成図</summary>

![構成図](image/lecture13/AWS.構成図.自動化処理図.drawio.png)
</details>

　　
- コードの詳細はこちらに記載しています
[課題で使ったリポジトリ](https://github.com/ReoNakamura/lecture13)

#### 事前準備
- ec2の接続に使うキーペアは事前に作成したものを使用しています

## circleciの環境変数の設定

##### Project Settings
![プロジェクトの設定](image/lecture13/circleciのプロジェクト設定.png)

##### Enviroment Varisbles
![環境変数の設定](image/lecture13/プロジェクト設定の環境変数.png)


## cirleci/comfig.ymlにansibleとserverspecの処理を追加する

### circleciの実行結果
1. 全てのワークフロー<br>![ワークフロー全体](image/lecture13/Workflowが全てsuccess.png)

2. cfn-lint<br>![cfn-lint成功](image/lecture13/cfn-lint成功.png)

3. execute-cloudformation<br>![cloudformston成功](image/lecture13/execute-cloudformation成功.png)

4. execute-ansible<br>![ansible成功](image/lecture13/execute-ansible成功.png)
![ansible成功2](image/lecture13/execute-ansible成功2.png)

5. execute-serverspec<br>![serverspec成功](image/lecture13/serverspec成功.pmg.png)

#### サンプルアプリケーションの動作確認
1. ALBのDNSにアクセスして画像をアップロード
![デプロイ](image/lecture13/デプロイ自動化.png)
2. 保存先がS3になっているか確認
![S3に保存](image/lecture13/保存先がS3になっている.png)

## 苦戦したところ
ansible-playbookを作るのに時間がかかってしまった。リモートで環境を構築するとき権限の問題や挙動がローカルでした時と違うので苦労した。

## 感想

cirrcleciなどのCI/CDツールとansibleを組み合わせると、コード管理やビルド・テストが素早くできて、もっと理解を深めて活用すれば開発に役立つとおもいました。
