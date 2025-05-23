## 自動販売機（データ構造と各種処理）のミニレポート
### Q5-1. 自動販売機の商品データついて説明せよ。
* データ構造（各項目とその説明）
*   ・itemsにはid,name,price,stockの4つの項目に分かれており、idは商品番号,nameは商品名,priceは金額,stockは在庫数が入っている。
* 連想配列の配列として定義するメリット
*   ・キーと値のペアでデータの格納しキーを使って直接要素にアクセスできるため、データの検索や操作を拘束に行えるのがメリット
### Q5-2. showItemListの処理内容について説明せよ。
* 配列の繰り返し処理
*   ・配列itemsの数だけ繰り返すループで内容は配列の各要素にアクセスしながらlogを 入力する.
* 連想配列の参照方法
*   ・items[c]が配列itemsの中の要素を指しており, for (let c in items)で配列のインデックス番号を取得し,items[c]で要素にアクセス,items.idなどで各キーに対応する値を参照
### Q5-3. buyItemの処理内容について説明せよ。
* 商品購入の可否判定
*   ・if (items[no-1].stock > 0)で在庫0なら購入できない
* 商品在庫を減らす処理
*   ・items[no-1].stock--;で購入したら在庫を1を表示
* 商品番号のエラー処理
*   ・if (no < 1|| items.length < no) {
                console.log("エラー:" + no + "は未設定の商品番号です。");
でifでnoが1より小さい値,または配列の長さより大きい数字はエラー表示する.
### Q5-4. プログラムの考察
* データ構造について
*   ・ 商品番号が並んでいるため処理が書きやすかったが番号が飛んだ場合は参照方法をかえなくてはならない
* 商品一覧表示と購入処理を関数化したメリット
*   ・一つの文章が長いので関数にすることによって文字数を減らすことができる
### Q5-5. 感想
* 今回の課題で苦労したこと
*   ・商品番号のエラー処理
* 演習を通して理解できたこと
*   ・基本的な文の書き方
* この自動販売機プログラムの追加機能や課題など
  ・先ほども述べた通り商品番号と配列が直接対応しない場合プログラムを変える必要がある.
* ・追加機能として一回で複数個変えるようにする.
