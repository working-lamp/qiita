---
title: Github Actions と Projects の連携
tags:
  - 'GithubActions'
private: false
updated_at: ''
id: null
organization_url_name: null
slide: false
ignorePublish: false
---
# タイトル後で考える

## この記事の内容

## Github Actions とは？

以下の記事を参考にまとめていきます。

https://qiita.com/shun198/items/14cdba2d8e58ab96cf95

できること: ビルド、テスト、デプロイなどの自動化
使い方: 
  1. `.github/workflows` ディレクトリ内にymlファイルを設置し、Workflow(ワークフロー)をファイル内に記述 → 指定した Event が発生すると実行される
	●	Workflow は Job 単位で分けられており、Job はさらに Step に分けられる。Step のなかには run コマンドが1つ以上ある
	●	Job は Runner という仮想マシンのインスタンス上で実行される 

用語

	●	jobs: 処理の最上位単位。jobsの中に1つ以上のジョブIDと共に処理が設定され、並列で実行される
	●	on: どのイベントが発生したら処理を実行するか指定
	●	runs-on: ジョブを実行するOS(ランナー)を指定
	●	uses: 他の人が作成した Action の読み込み
	●	steps: Workflow は Job 単位で分けられており、Job はさらに Step に分けられる。Step のなかには run コマンドが1つ以上ある
	●	run: 実行するコマンド。name には run の処理内容を書き、Github 上で確認することができる。複数以上のコマンドを実行したい時は run　| と記載
	●	env: 環境変数
	●	secrets: 見られたくない環境変数
	●	サービスコンテナ: ワークフローを実行する際に必要になるサービスを使用するためのDockerコンテナ（??）
	●	options: 実行したい任意のコマンド。DBやRedisなどのインメモリキャッシュとの接続の際はヘルスチェックコマンドを記載する（??）
	●	スコープ: 権限。read, write, none がある


## Github Projects とは？

## Actions と Projects を連携させると何ができる？

## Github Actions のセットアップ

## 結論