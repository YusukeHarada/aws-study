# AWS 学習ロードマップ

## 全体フロー

```mermaid
flowchart TD
    A["✅ IAM / セキュリティ設定"] --> B["✅ VPC 作成"]
    B --> C["✅ S3 静的ホスティング"]
    B --> D["✅ EC2 + Nginx"]
    D --> E["✅ Docker on EC2"]
    C --> F["🔄 CloudFront (HTTPS)"]
    A --> G["🔄 AWS CLI セットアップ"]
    G --> H["🔄 API Gateway + Lambda"]
    H --> I["⬜ DynamoDB"]
    F & H & I --> J["⬜ ToDoリスト API 完成"]
    E --> K["⬜ ECR"]
    K --> L["⬜ ECS + Fargate"]
    L --> M["⬜ ALB"]
    J & M --> N["⬜ CloudFormation"]
    N --> O["⬜ AWS SAM"]
    J --> P["⬜ CloudWatch / X-Ray"]
```

> 凡例: ✅ 完了 / 🔄 学習中 / ⬜ 未着手

---

## フェーズ別スケジュール

```mermaid
gantt
    title AWS 学習スケジュール（目安）
    dateFormat  YYYY-MM-DD
    section Phase 1: サーバーレス API
    AWS CLI セットアップ       :p1a, 2026-06-22, 3d
    API Gateway + Lambda       :p1b, after p1a, 5d
    DynamoDB                   :p1c, after p1b, 5d
    CloudFront                 :p1d, after p1b, 4d
    ToDoリスト API 統合        :p1e, after p1c, 3d
    section Phase 2: コンテナ
    ECR                        :p2a, after p1e, 3d
    ECS + Fargate              :p2b, after p2a, 7d
    ALB                        :p2c, after p2b, 4d
    section Phase 3: IaC
    CloudFormation             :p3a, after p2c, 7d
    AWS SAM                    :p3b, after p3a, 5d
    section Phase 4: 監視
    CloudWatch / X-Ray         :p4a, after p3b, 7d
    Cost Explorer              :p4b, after p4a, 3d
```

---

## 前提スキルの依存関係

| 学ぶトピック | 必要な前提知識 |
|-------------|---------------|
| API Gateway + Lambda | Lambda 基本 ✅ |
| DynamoDB | Lambda + API Gateway |
| CloudFront | S3 静的ホスティング ✅ |
| ECR | Docker on EC2 ✅ |
| ECS + Fargate | ECR, VPC ✅ |
| CloudFormation | 各サービスの手動操作経験 |
| AWS SAM | Lambda, API Gateway, CloudFormation |
| CloudWatch | Lambda or EC2 ✅ |
| X-Ray | Lambda + API Gateway |

---

## マイルストーン

| マイルストーン | 達成条件 |
|---------------|---------|
| 🏆 サーバーレス入門 | ToDoリスト API (API GW + Lambda + DynamoDB) が動作する |
| 🏆 コンテナ運用 | Fargate + ALB でコンテナが HTTPS 公開される |
| 🏆 IaC 入門 | CloudFormation で構成を再現できる |
| 🏆 AWS 実践レベル | 監視・コスト管理まで含めた運用ができる |
