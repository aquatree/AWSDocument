# X-Ray

* アプリやアプリ基盤を分析し、エラーや問題の原因を特定できるサービス
  
## できること

* サービスマップの作成
  * アプリケーションに対するリクエストが追跡され、アプリケーションによって使用されるサービスマップが作成される
  * アプリケーション内のサービス間のつながりを把握できる
  * 依存性ツリーの作成
  * 複数の AWS アベイラビリティゾーンまたはリージョン間で発生するレイテンシーやエラーの検出
  * 正常に実行されていないサービスの把握
* エラーとバグの特定
  * アプリケーションに対する各リクエストの応答コードが分析され、アプリケーション内のバグやエラーが自動的に検出
  * バグやエラーを再現することなく、アプリケーションコードを簡単にデバッグ
* 独自の分析と可視化アプリケーションの作成
  * X-Ray で用意されたクエリ API のセットを使用して、X-Ray で記録されたデータに基づく独自の分析や可視化のためのアプリケーションを構築

## トレース

* クライアントからリクエストが作成されると、一意のトレースIDが割り振られる
* リクエストがアプリケーションに入ると、トレースIDによってX-Rayに情報がいく
  * ↑これら情報のひとつひとつがセグメント。トレースはセグメントの集合体

## セグメント

* システム定義のデータとユーザ定義のデータが注釈の形で含まれる
* 1つ以上のサブセグメントで構成
* サブセグメントにはクエリ、使用されたテーブル、タイムスタンプ、エラーステータスなどのデータが含まれる

## 注釈（アノテーション）

* 追加情報を記録できるキーバリュー型
* フィルター式で使用するためのインデックスを記載できる

## メタデータ

* トレースに保存する追加のデータを記載できる（フィルター式で使用するインデックスは記載できない）

## サンプリングの計算

* 1秒あたりx回のリクエストをサンプリングする場合
  * x= リザーバサイズ + ((1秒あたりの全リクエスト-リザーバサイズ)*固定レート)
