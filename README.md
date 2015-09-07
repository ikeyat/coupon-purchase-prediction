# coupon-purchase-prediction
https://www.kaggle.com/c/coupon-purchase-prediction/data
をいつかやるかもしれないので、
思ったことをメモしておく。

## 理解メモ
 * 推薦システムとしてせめるなら
    * 内容ベースでやるか、協調フィルタリングでやるか？
       * テスト対象クーポンが学習データにない場合は内容ベースでやるしかない
           http://gihyo.jp/dev/serial/01/information-recommendation-system/0003?page=2
       * サンプリングして何個か調べたところテスト対象クーポンは学習データに含まれていなかった。内容ベースでやる。
 * 機械学習？
    * モデルは簡単に作れそう   
 * 全ユーザに対して最適な1クーポンを推薦する、と言うのが目的？
    * 全ユーザに対して最適10クーポン予測して、Mean average precisionをとる。
      意訳すると、なるべくランキング上位にたくさん購入したクーポンを当てればよい。
      https://www.kaggle.com/c/coupon-purchase-prediction/details/evaluation
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
 * Relation数（ユーザ-クーポン）は2833181の模様

## TODO
 * テスト対象クーポンが学習データに含まれているか確認する
    * done. 含まれていなかった。
 

## 参考
* 機械学習の復習
   http://gihyo.jp/dev/serial/01/machine-learning
* 推薦システムのまとめ的な論文
   http://soc-research.org/ja/wp-content/uploads/2014/08/IFSurvey4IPSJ.pdf
* Rで単純ベイズ分類器
   https://sites.google.com/site/yusukekikuchiwebsite/memo/nbiris
