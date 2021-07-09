# 業務経歴書

## 基本情報

|key|value|
|----|----|
|名前|洞口 鎮吾|
|住所|埼玉県|


## 概要

- クラウドアーキテクチャ設計、クラウドインフラ構築管理、基盤コード開発、DevOpsが現在の専門です。
- バックエンドの多種多様な言語/DB/フレームワークを用いた豊富な開発経験があり、AWSの様々なマネージドサービスに精通しています。
- 元々はWindows系のエンジニアなので.NET系の開発も経験しておりますが現在はLinuxプラットフォームでの開発がメインです。


## スキル

- 基本的にすべて実業務で使用した技術だけを列挙しています。

### 言語

Go | Ruby | Python | PHP | JavaScript | VB.NET


### フレームワーク等

Ruby on Rails | CakePHP | jQuery | .NET Framework

### RDB/NoSQL

MySQL | PostgreSQL | Oracle | SQL Server | Redis | Memcached

### AWS

VPC | S3 | Cloud Front | API Gateway | Lambda | ELB | EC2 | ECS | Fargate | Route53 | IAM | Elasticsearch Service | RDS(MySQL|PostgreSQL) | Aurora | DynamoDB | ElastiCache(Redis) | Kinesis firehose | SNS | SES | Cloud Watch | CloudTrail | GuardDuby | KMS | CodePipeline | CodeBuild | CodeDeploy | ECR | WAF


### SaaS/PaaS

GitHub | Backlog | GitLab | DataDog | NewRelic | TreasureData


### その他

Terraform | Docker | Jenkins | Fluentd | Capistrano | Chef | nginx | unicorn | Apache | Tomcat | Elasticsearch | Kibana | IIS | Active Directory


## バリューを発揮しやすい業務

- クラウドアーキテクチャ設計
- クラウドインフラ構築管理
- local/dev/stg/prd環境の適切な切り分け
- Gitブランチモデルの適切な定義
- サーバーレスアーキテクチャの導入
- メッセージングサービスの導入
- CDNの導入
- CIサービスの導入
- コンテナ化(Docker化)
- インフラのコード化
- オートスケールの設定
- デプロイの自動化
- データベースマイグレーションの自動化
- バッチジョブのフロー制御
- クラウドの権限管理
- 監視ダッシュボードの導入

## 主な業務経歴

### 医療分野におけるPHR(Personal Health Record)サービスのアーキテクチャ設計/インフラ構築/DevOps基盤構築【Go/ECS/GitOps/CodePipeline/Terraform/AWS】(2020年〜)

【プロジェクト概要】PHRサービスの新規開発チームにおいて、インフラの構築/DevOps基盤構築、技術検証用アプリケーションの開発作業等を担当

【担当業務】
Terraformによるインフラのコード化、CodePipelineを使用したGitOpsスタイルのCI/CDパイプラインの構築、各種自動化スクリプトの作成、バッチジョブの作成等を担当。具体的には下記。
- Terraformによるインフラのコード化(VPC/ECS/Fargate/Aurora/CloudFront等)
Terraformを使用したインフラのコード化を行うことで、バージョン管理や他のプロジェクトでも再利用できる形にし、開発効率の利便性が向上されました。
- ECS(Fargate)を使用したサービス基盤の構築
社内で採用がなかったECS/Fargateを0から検証を兼ねて使うことになりました。
FargateのデメリットであるパプリックIPの固定割り当てが出来ない問題はNAT ゲートウェイを利用することによりIPアドレスを固定化させ、コンテナアクセスをサポートしていない問題はECS Execを利用しコンテナ内でのコマンドを実行できるようにしました。
- CodePipelineのECS環境での構築およびPipelineとArtifacts機能を使用したCDパイプラインのコード化
当初はJenkinsを導入検討していましたが、1日数回しか使わないサーバを稼働させるコストと運用の手間が惜しくなり、CodePipeline、CodeBuild、CodeDeployを利用してサーバレスな仕組みを構築しました。これによりコストダウンでき、サーバ運用の手間から解放されました。
- BacklogとCodepipelineの連携によるGitOpsスタイルのCI/CDパイプラインの構築
- SESによるメール配信基盤の構築
- SNSによるSMS(ショートメッセージ)配信基盤の構築
- Chatbotを使用してAWSからのイベントをSlackへ通知
- マネージドルールと独自のルール(Geo Matchルール、レートベースのルール等)を組み合わせてWAFを構築
- CloudWatch + ECS タスクスケジューラによる各種バッチジョブの作成
- 上記の様々な機能が実装された技術検証用アプリケーション(Nginx + Go)の作成と本体アプリケーションへの機能の組み込み

【発揮したバリュー】
これまでの案件で培ったAWSやDevOpsの知見を活かし、インフラのコード化やCI/CDパイプラインの構築、各種自動化作業等に大きく貢献。CodePipelineは初体験であったがPipelineやArtifacts等の機能を速習して短期間でキャッチアップ。


### スマートフォン向けゲームサービスのインフラ構築 /DevOps基盤構築【Kotlin/Java/ECS/Terraform/AWS】(2019年~2020年)

【プロジェクト概要】
スマートフォン向けゲームサービスの新規開発チームにおいて、インフラの構築管理、基盤コードの作成作業等を担当

【担当業務】
Terraform、Ansibleによるインフラのコード化、各種デプロイスクリプトの作成等を担当。具体的には下記。
- Terraform、Ansibleによるインフラのコード化(VPC/ECS/EC2/Backup/ElastiCache/Aurora等)
Terraformを使用したインフラのコード化を行うことで、バージョン管理や他のプロジェクトでも再利用できる形にし、開発効率の利便性が向上されました。
- TerraformからDatadogで、監視定義コード化とgit管理
Terraformを使用した監視定義のコード化を行い、バージョン管理や他のプロジェクトでも再利用できる形にし、開発効率および運用・監視定義更新の利便性が向上されました。
- DatadogとAWSのインテグレーションとモニタリング
- ECS、EC2を使用したサービス基盤の構築
- AWS CLIを利用して検証環境のサーバー停止、起動のスクリプトを作成
- 検証環境のサーバー停止、起動のスクリプトをJenkinsでスケジューリング
- Trusted Advisorによるコスト最適化

【発揮したバリュー】
Terraform、AnsibleによるAWSのインフラ構築と管理作業等を担当。Terraform、Ansibleは初体験であったが短期間でキャッチアップ。 またAWSサポート等を有効に活用して適切なAWSサービスを選択/提案しサービス全体のシンプル化に貢献。AWSを本格的に使用するのはこれが初体験であったが、短期間でキャッチアップ。様々な情報を参考にしてその時点のベストプラクティスな手法やライブラリを入念に調査＆積極的に採用し、良い意味でコモディティ化された保守性の高い構成を実現。



