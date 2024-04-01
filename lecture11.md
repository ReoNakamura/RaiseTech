# 第11回課題
## ServerSpecを使ってテストの自動化を行う
- テスト項目を自分なりにカスタマイズしてテストを成功させること
### ServerSpecのインストール

- ディレクトリを作成する  

```bash
＄mkdir server-spec-sample

#ディレクトリ移動
＄cd server-spec-sample

#gemfile作成
＄bundle init

#作成された空のgemfileに下記を追記
＄gem 'serverspec'
#インストール
＄bundle install
```
### ServerSpecのセットアップ
```bash
#osと接続方法の選択
＄serverspec-init
#対話式なので1.2を選択する
Select OS type:

  1) UN*X　　　#linuxなど
  2) Windows

Select number: 1

Select a backend type:

  1) SSH
  2) Exec (local)

Select number: 2

```
- セットアップが終わると以下のディレクトリとファイルが生成される
```bash
#どんなテストをするかが記載されているファイルが中にあるディレクトリ
+ spec/
#テスト項目を記載するファイル
+ spec/localhost/sample_spec.rb

#テストで最初に読み込まれるファイルで全体で共通の設定を定義するのに適している
+ spec/spec_helper.rb

#rakeコマンドでテストを行うので実行処理が書かれている
+ Rakefile

+ .rspec

 ```
 ### テスト項目
 - 提供されてサンプルテストコードにテスト項目をいくつか追加して行った
 - /home/ec2-user/server-spec-sample/spec/localhost/sample_spec.rbの中身

```bash

require 'spec_helper'
#80番ポートの指定
listen_port = 80
#nginxがインストールされているか
describe package('nginx') do
  it { should be_installed }
end
#[追加テスト]rubyが指定のバージョンかどうか
describe command('ruby -v') do
  its(:stdout) { should match /ruby 3\.1\.2/ }
end
#[追加テスト]nginxが起動しているか
describe service('nginx') do
  it { should be_running }
end
#[追加テスト]nginxが指定のバージョンか
describe package('nginx') do
  it { should be_installed.with_version('1.22.1') }
end
#[追加テスト]3306番ポートをlistenしているか
describe port(3306) do
    it { should be_listening }
end
#[追加テスト]　mysqlが起動しているか、自動起動がついてるか
describe service('mysqld') do
  it { should be_enabled   }
  it { should be_running   }
end
#指定したポートをlistenしているか
describe port(listen_port) do
  it { should be_listening }
end
#curlコマンドでHttpでアクセスして200 okが帰ってくるか
describe command('curl http://127.0.0.1:#{listen_port}/_plugin/head/ -o /dev/null -w "%{http_code}\n" -s') do
  its(:stdout) { should match /^200$/ }
end

```
## テスト実行
- テスト成功
![テスト成功](/image/lecture11/テスト成功.png)
- nginxを停止  
  テスト失敗
![テスト失敗](/image/lecture11/テスト失敗.png)

### 学んだこと
- インフラ環境がちゃんと動作してるか確認が必要な事と、手動ではミスも起きるし効率もわるいのでテスト自動化ツールを使って用途に合わせてテストする事を学べた。  
簡単なテストしか出来ていないと思うので仕組みをしっかり理解して細かいテストコードも書けるよう頑張っていきたいとおもった。