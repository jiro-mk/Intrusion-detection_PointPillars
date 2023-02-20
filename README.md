# 3次元点群での人物検出と侵入検知 (Intrusion-detection_PointPillars)

RGBカメラと違い、3Dセンサは暗部でも撮影可能

→夜間や照明が少ない環境でも正常に作動させることができる

## 追加機能(2023/2)

・検出したオブジェクトの個数、時間、バウンディングボックスの位置をフレーム毎に出力

・検出対象オブジェクトの追加（自転車、自動車）

## 処理

・人物検出

PointPillarsを使用

→Lidarで取得した点群から人物を高速で検出可能


・侵入検知

3次元で定義したエリア内で人物が検出された人物のみバウンディングボックスで囲んで可視化


Quick hullを実装し、人物の点群と定義エリアの頂点を用いて内外判定を行う



・PointPillarsの検出例

参考：https://github.com/zhulf0804/PointPillars

![image](https://user-images.githubusercontent.com/93971055/188312175-5021ccd5-faf3-4981-8b9d-fdba1706a9f5.png)


## 侵入検知デモ

青色で囲まれたエリアが侵入検知をするエリアであり、

エリア内で検出された人物だけが黄色のバウンディングボックスで囲まれて表示されているのが分かる。

![image](https://user-images.githubusercontent.com/93971055/188312222-2a5762dc-0fd0-4d49-ba04-5f5443cac8e9.png)

![image](https://user-images.githubusercontent.com/93971055/188312236-a56066cc-89e0-4fe5-b9d2-e5b4588b63e1.png)


〇出力
・csvの例

![image](https://user-images.githubusercontent.com/93971055/220100814-8eb912c3-d7cc-45a8-beba-f52d7f09c580.png)


・フレームごとのカウント出力

--

--


## Author

jiro-mk

