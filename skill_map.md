# AWS スキルマップ

## 現在の習熟状況

> ✅ 完了 / 🔄 学習中 / ⬜ 未着手

### セキュリティ・認証

| サービス / スキル | 状況 | 備考 |
|------------------|------|------|
| IAM ユーザー作成・管理 | ✅ | 管理者ユーザー作成済み |
| MFA 設定（root / IAM） | ✅ | Google Authenticator 設定済み |
| IAM ポリシー・権限設計 | 🔄 | AdministratorAccess のみ |
| IAM ロール | ⬜ | Lambda 実行ロール含む |
| AWS Organizations | ⬜ | マルチアカウント管理 |

### ネットワーク

| サービス / スキル | 状況 | 備考 |
|------------------|------|------|
| VPC 作成・設計 | ✅ | CIDR 10.0.0.0/16 |
| サブネット（パブリック / プライベート） | 🔄 | パブリックのみ |
| セキュリティグループ | ✅ | HTTP/SSH 許可 |
| インターネットゲートウェイ | 🔄 | 暗黙的に使用 |
| NAT ゲートウェイ | ⬜ | プライベートサブネット用 |
| Route 53 | ⬜ | DNS 管理 |
| CloudFront | 🔄 | S3 HTTPS 化（未完了） |
| ALB | ⬜ | ECS/Fargate 連携 |

### コンピュート

| サービス / スキル | 状況 | 備考 |
|------------------|------|------|
| EC2 インスタンス作成・操作 | ✅ | t2.micro, SSH 接続 |
| EC2 キーペア管理 | ✅ | |
| Lambda 関数作成・テスト | ✅ | Python 3.12 |
| Lambda トリガー設定 | 🔄 | API GW 連携未完了 |
| Lambda 環境変数・設定 | ⬜ | |
| ECS + Fargate | ⬜ | |
| Auto Scaling | ⬜ | |

### ストレージ

| サービス / スキル | 状況 | 備考 |
|------------------|------|------|
| S3 バケット作成・操作 | ✅ | 静的ホスティング設定済み |
| S3 バケットポリシー | ✅ | パブリック読み取り許可 |
| S3 バージョニング | ⬜ | |
| ECR | ⬜ | Docker イメージ管理 |
| EFS | ⬜ | 共有ファイルシステム |

### データベース

| サービス / スキル | 状況 | 備考 |
|------------------|------|------|
| DynamoDB テーブル作成 | ⬜ | |
| DynamoDB CRUD 操作 | ⬜ | |
| RDS | ⬜ | リレーショナル DB |
| ElastiCache | ⬜ | Redis/Memcached |

### API・統合

| サービス / スキル | 状況 | 備考 |
|------------------|------|------|
| API Gateway REST API | 🔄 | Lambda 連携未完了 |
| API Gateway HTTP API | ⬜ | |
| SQS | ⬜ | メッセージキュー |
| SNS | ⬜ | 通知サービス |
| EventBridge | ⬜ | イベント駆動 |

### インフラ as Code

| サービス / スキル | 状況 | 備考 |
|------------------|------|------|
| AWS CLI | 🔄 | インストール未完了 |
| CloudFormation | ⬜ | |
| AWS SAM | ⬜ | |
| CDK | ⬜ | TypeScript/Python |
| Terraform (AWS Provider) | ⬜ | |

### 監視・運用

| サービス / スキル | 状況 | 備考 |
|------------------|------|------|
| AWS Budgets | ✅ | 月次コストアラート設定済み |
| CloudWatch ログ | ⬜ | |
| CloudWatch メトリクス・アラート | ⬜ | |
| CloudWatch ダッシュボード | ⬜ | |
| X-Ray | ⬜ | 分散トレーシング |
| Cost Explorer | ⬜ | |

### コンテナ・DevOps

| サービス / スキル | 状況 | 備考 |
|------------------|------|------|
| Docker 基本操作 | ✅ | EC2 上で実行済み |
| Docker Compose | ⬜ | |
| ECR へのプッシュ | ⬜ | |
| ECS タスク定義 | ⬜ | |
| CodePipeline / CodeBuild | ⬜ | CI/CD |
| GitHub Actions + AWS | ⬜ | |
