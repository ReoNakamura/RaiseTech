# 第６回課題

## cloud Trailを使って証跡を取る
- cloud trailを有効化
![cloudTrailイベント](lecture06/cloudTrailイベント.png)
##### イベント名         
1. StartDBInstance
![StartDBInstance](lecture06/StartDBInstance.png)
2. StartInstances
![StartInstances](lecture06/StartInstances.png)
3. StopDBInstance
![StopDBInstance](lecture06/StopDBInstance.png)
## アラートの設定
- アラートを設定するにはAmazonSNSでプッシュ通知を受信するメールを設定する
- AmazonSNSでトピック作成
![AmazonSNSでトピック作成](lecture06/AmazonSNSでトピック作成.png)
- サブスクリプション作成
![サブスクリプション作成](lecture06/サブスクリプション作成.png)
###### cloud Watchでアラート作成

![アラートの設定](lecture06/アラートの設定.png)
![アラート設定条件](lecture06/アラート設定条件.png)
- アラート
![testAleart](lecture06/testAleart.png)
- アクション
![アクション](lecture06/アクション.png)

- アラート作成時にamazonSNSで設定したプッシュ通知が送られるメールを設定する
### アラートの確認
-状態ok->alarm
![状態ok->alarm](lecture06/状態ok->alarm.png)

- 状態　alarm->ok
![状態アラーム->ok](lecture06/状態アラーム->ok.png)
# AWS 利用料の見積もり
- 見積書 
https://calculator.aws/#/estimate?id=f4ecb1fed3ddf1f53a148f66a055c813b45f4a39

- 現在の利用料
![billingのホーム](lecture06/billingのホーム.png)
- EC2の利用料金
![ec2利用料金](lecture06/ec2利用料金.png)
### 感想
- 消費税込みで719円の請求ですこし無料枠を超えた。
- エンジニアになり実際に仕事をしていく上でログがどれほど大切か分かった

- 第５回に比べるとデモンストレーションを見ながらスムーズにできた

