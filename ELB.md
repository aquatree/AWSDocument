# Elastic Load Balancing

* ALB, NLB, CLBの総称
* EC2インスタンス、コンテナ、IPアドレス、Lambda関数等へのトラフィックを分散する

## ALB(Application Load Balancer)

* http, https のトラフィックの負荷を分散し、マイクロサービスやECSなどに処理を振り分ける
* レイヤ7で動作する

## NLB(Netwaork Load Balancer)

* http, https以外は基本的にこちらを使用する
* 数百万リクエストといった大規模なトラフィックでも拘束に不可を分散させることが可能（ALBより高い性能）
* レイヤ4で動作する

## CLB(Classic Load Balancer)

* 旧タイプのロードバランサー
* EC2-Classicネットワークなど、後方互換性のために残されている
* レイヤ4, 7で動作する