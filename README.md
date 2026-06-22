# AWS ハンズオン学習記録

AWSを実践的に学ぶためのハンズオン手順書と学習記録です。

## 対象者

- AWSの基礎を学びたい方
- EC2など一部の経験はあるが、現代的なAWSの使い方を習得したい方
- サーバーレス構成（S3・Lambda・API Gateway・DynamoDB）に入門したい方

## 構成

```
.
└── aws_handson_guide.md    # ハンズオン手順書
```

## 手順書の内容

| # | 内容 |
|---|---|
| 1 | AWSアカウントのセキュリティ初期設定 |
| 2 | IAMユーザーの作成 |
| 3 | 請求アラートの設定 |
| 4 | VPCの作成 |
| 5 | S3静的ホスティング |
| 6 | Lambda関数の作成 |
| 7 | EC2インスタンスの作成とSSH接続 |
| 8 | NginxをEC2上で起動する |
| 9 | DockerをEC2にインストールする |
| 10 | EC2インスタンスの停止 |

## 前提条件

- AWSアカウントが作成済みであること
- Mac / Linux 環境のターミナルが使えること
- ブラウザからAWSマネジメントコンソールにアクセスできること

## 次のステップ

- [ ] API Gateway + Lambdaの連携
- [ ] DynamoDBでデータを保存する
- [ ] AWS CLIをMacにセットアップする
- [ ] CloudFrontでS3をHTTPS化する
- [ ] ECS / Fargateでコンテナを運用する

## 参考リンク

- [AWS公式ドキュメント](https://docs.aws.amazon.com/ja_jp/)
- [AWS無料利用枠](https://aws.amazon.com/jp/free/)
- [AWS Well-Architectedフレームワーク](https://aws.amazon.com/jp/architecture/well-architected/)
