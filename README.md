# AWS個人学習の内容
クラウド関連の業務経験が無いので、
それを補うため以下の学習を行いました。

## AWS座学
2023年9月にSAAを取得。

## AWS実技

### 1.　マネージメントコンソールから以下構成を作成

- マネージメントコンソールからAWSリソース（VPC, ALB, EC2, RDS, S3, IAM）を作成
- EC2にアプリサーバ環境構築　（Rails + Nginx + Unicorn + mysql）

##### 構成図
![diagram-management-console.png](./images/diagram-management-console.png)

### 2.　CloudFormationについて学習
- CloudFormationテンプレートから上記AWSリソース（VPC, ALB, EC2, RDS, S3, IAM）を自動作成

### 3.　circleciからCloudFormaiton,Ancibleを使ってWEBアプリが動かす
- circleci、Ansibleを学習し、以下のものを作成しました。

  - GitHubにpushを行うだけでcircleciが以下を自動実行

    1. CloudFormationでAWSリソース( VPC, ALB, EC2, RDS, S3, IAM ) を作成
    2. AnsibleでWEBアプリサーバ環境構築 ＋ ソースコードをデプロイ
    3. ServerspecでWEBページ表示テスト

##### 構成図
![diagram.png](./images/diagram.png)

- circleの全タスクが正常終了
![circleci-all-tasks.png](./images/circleci-all-tasks.png)

- 新規投稿した結果
![new-fruits-result.png](./images/new-fruits-result.png)


- バケットに画像が保存されていることを確認
![s3bucket.png](./images/s3bucket.png)




#### ソースコード

.circleci/config/yml
cloudformationテンプレート
ansible
sshconfig


## 今後の学習したいもの
- 以下機能の実装
  - Auto Scaling　（とりあえず動かしたが実務レベルの設計はまだ）
  - SNS,SQS, API Gateway、Lambda関数
  - TerraForm
  - 複雑なシェルスクリプト、
  - コンテナ技術（ECS,EKS,Kubernetes)
  - 監視・運用関連の技術
  - などなど


- 資格
  - SAP　(Solutions Architect - Professional)
  - SOA  (SysOps Administrator Associate)
  - DVA  (Developer Associate)
  - SCS(セキュリティ)
  - ANS（ネットワーク）
  - 応用情報処理
  - 情報安全確保支援士

- その他
  - AWSの設計関連書籍を読む
