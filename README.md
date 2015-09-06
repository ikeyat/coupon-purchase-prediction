# coupon-purchase-prediction
https://www.kaggle.com/c/coupon-purchase-prediction/data
をいつかやるかもしれないので、
思ったことをメモしておく。

## 理解メモ
 * 内容ベースでやるか、協調フィルタリングでやるか？
    * テスト対象クーポンが学習データにない場合は内容ベースでやるしかない
        http://gihyo.jp/dev/serial/01/information-recommendation-system/0003?page=2
 * 全ユーザに対して最適な1クーポンを推薦する、と言うのが目的
    * ユーザベースで解析した方が良さそう
 * 内容ベースでやる場合
    * ユーザ
      * 地域
      * 年齢
      * 性別
    * クーポン
      * 地域  
      * ジャンル
      * 価格
      * 割引率
 * ユーザの登録日以前のクーポンは学習対象に入れないべき
 
## TODO
 * テスト対象クーポンが学習データに含まれているか確認する
