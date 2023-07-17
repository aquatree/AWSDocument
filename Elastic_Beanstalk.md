# AWS Elastic Beanstalk

## カスタムAMI

* 標準のElastic Beanstalk AMI の代わりにAmazon AMIを指定できる。
* 標準AMIに含まれていない依存関係を事前にロードしてあるAMIを指定することで、デプロイが短縮される
* 設定ファイルの使用もデプロイを短縮できるが、更新時に時間がかかることがある
