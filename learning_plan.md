# AWS 学習プラン

## 現在地

`aws_handson_guide.md` で以下を完了済み:
- IAM / MFA / セキュリティ初期設定
- VPC 作成
- S3 静的ホスティング
- Lambda 基本実装
- EC2 + Nginx + Docker

---

## Phase 1: サーバーレス API の完成（目安: 2〜3週間）

**ゴール:** API Gateway → Lambda → DynamoDB の完全なサーバーレス Web API を構築する。

### ステップ

| # | トピック | 内容 |
|---|----------|------|
| 1 | AWS CLI セットアップ | ローカルPCにCLIをインストールし、IAMユーザーの認証情報を設定する |
| 2 | API Gateway + Lambda | REST APIエンドポイントを作成し、URLからLambdaを呼び出す |
| 3 | DynamoDB 基本 | テーブルを作成し、Lambda から Put/Get/Query 操作を行う |
| 4 | CloudFront | S3 静的サイトに CloudFront を被せて HTTPS + CDN を実現する |

**成果物:** 「ToDoリスト API」
- `POST /todos` → DynamoDB に保存
- `GET /todos` → 一覧取得
- S3 のフロントエンドから API を呼び出す

---

## Phase 2: コンテナオーケストレーション（目安: 2〜3週間）

**ゴール:** EC2/Docker の知識を ECS/Fargate に発展させ、マネージドなコンテナ環境を構築する。

### ステップ

| # | トピック | 内容 |
|---|----------|------|
| 1 | ECR | Docker イメージをプライベートレジストリにプッシュする |
| 2 | ECS + Fargate | サーバーレスでコンテナを実行する（EC2の管理不要） |
| 3 | ALB | Application Load Balancer でコンテナにトラフィックを分散する |

**成果物:** Fargate 上の Nginx コンテナを ALB 経由で HTTPS 公開

---

## Phase 3: インフラ as Code（目安: 2週間）

**ゴール:** 手動操作から脱却し、コードで再現性のあるインフラを管理する。

### ステップ

| # | トピック | 内容 |
|---|----------|------|
| 1 | CloudFormation 基本 | YAML テンプレートで VPC / EC2 / S3 を定義する |
| 2 | AWS SAM | Lambda / API Gateway のローカル開発・テスト・デプロイを自動化する |

**成果物:** Phase 1 の ToDoリスト API 構成を CloudFormation + SAM で再現

---

## Phase 4: 監視・運用（目安: 1〜2週間）

**ゴール:** 本番運用を意識した監視・ログ・コスト管理を習得する。

### ステップ

| # | トピック | 内容 |
|---|----------|------|
| 1 | CloudWatch | ログ収集、メトリクスダッシュボード、アラート設定 |
| 2 | X-Ray | Lambda / API Gateway の分散トレーシング |
| 3 | Cost Explorer | コスト分析とリソース最適化 |

---

## 参考ドキュメント

- [ロードマップ](roadmap.md) — フェーズ別の学習フロー図
- [スキルマップ](skill_map.md) — AWS サービス別の習熟状況一覧
- [スキルレベル基準表](skill_level_criteria.md) — 各スキルの習熟度定義
- [ハンズオン手順書](aws_handson_guide.md) — 実際の操作手順
