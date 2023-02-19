# Dynamodb

* Dynamodb ストリーム
  * 有効にすると、更新などDynamodbのイベントをトリガーとして、Lambda関数などを実行できる
    * INSERT: アイテム新規作成
    * MODIFY: 既存アイテムに属性を新規追加、または既存アイテムの既存キーの値を変更
    * REMOVE: 既存アイテムを削除
  * アクセスできるデータは24h以内に変更されたもの
  * 以下の4種類の表示タイプ（StreamViewType）がある
    * KEYS_ONLY: 変更されたキー属性のみ
    * NEW_IMAGE: 変更後に表示される項目全体
    * OLD_IMAGE: 変更前に表示されていた項目全体
    * NEW_AND_OLD_IMAGES: 新しいイメージと古いイメージの両方