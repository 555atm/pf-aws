# pf-aws
portforio of aws learning
クラウド関連の業務経験は無いため、
それを補うため以下の学習を行いました。

## AWS座学
2023年9月にSAAを取得。

## AWS実技

### ①　マネージメントコンソールで以下構成を作成

[図]
VPC
ALB
EC2（nginx + unicorn + Rails）
RDS(mysql)
S3(webアプリ上の画像を保存)

### ②　CloudFormationについて学習
- 上記構成をCloudFormationで作成
（図は載せない）

### ③　circlciからcloudformaiton,Ancibleを使ってWEBアプリが動かす

GitHubにpushを行うとcircleciが以下を実行

　① CloudFormationでAWSリソース( VPC, ALB, EC2, RDS, S3, IAM ) を作成
　② AnsibleでWEBアプリサーバ環境構築 ＋ ソースコードをデプロイ
　③ ServerspecでWEBページ表示テスト

#### 構成図
![diagram.png](./images/diagram.png)

#### ソースコード
.circleci/config/yml
cloudformation
ansible
sshconfig
rails


## 今後の学習予定
- 実技
  - teraform
  - Auto Scaling
  - SNS+SQS
  - ECS,EKS
  - 監視・運用関連
  - （（　複雑なシェルスクリプト　））
  - などなど


- 資格
  - SAP　(Solutions Architect - Professional)
  - SOA  (SysOps Administrator Associate)
  - DVA  (Developer Associate)
  - セキュリティ
  - NW
  - 応用情報

- その他
  - AWSの設計関連書籍を読む