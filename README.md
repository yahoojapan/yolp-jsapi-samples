Yahoo! JavaScriptマップAPIサンプルコード集
==========================================

概要
----

Yahoo!デベロッパーネットワークで提供している[Yahoo! Open Local Platform](http://developer.yahoo.co.jp/webapi/map/)のAPI/SDK群の一つ、[Yahoo! JavaScriptマップAPI](http://developer.yahoo.co.jp/webapi/map/openlocalplatform/v1/js/)を中心に作成されたWebアプリケーションのサンプルコード集です。

使い方
------

### 1. アプリケーションIDの登録

Yahoo!デベロッパーネットワークで[アプリケーションIDを登録](https://e.developer.yahoo.co.jp/webservices/register_application)して下さい。

既に登録済みの方は、次へ進んで下さい。

### 2. サンプルコード集の入手

* Gitを利用できる環境にある方は、次に示すコマンドでリポジトリを取得して下さい。
* Windows用のGitフロントエンドツールであるTortoiseGitを利用している方も、コマンド同様の場所から複製を入手して下さい。
* Gitを利用できる環境でない方は、ZIPアーカイブ形式で入手し、展開して下さい。

(リポジトリの取得)

    $ git clone git://github.com/yahoojpYOLP/yolp-jsapi-samples.git

### 3. アプリケーションIDの埋め込み

自分で登録・管理しているアプリケーションIDを、各サンプルコードのHTMLファイルに埋め込んで下さい。

各サンプルコードでは埋め込む箇所に「YourApplicationId」と記述されています。ご利用のテキストエディタ等で置換するか、UNIX系OSであれば、以下のように「登録したアプリケーションID(ここでは例としてOpenLocalPlatform)」へ書き変えてください。

(自分で登録したアプリケーションIDへの書き換え)

    $ cd yolp-jsapi-samples
    $ find . -type f -name "*.html" -print0 | xargs -0 perl -pi -e "s/YourApplicationId/OpenLocalPlatform/g"

### 4. 動作確認

アプリケーションIDを埋め込んだHTMLファイルを直接ウェブブラウザから開くことで動作が確認できます。

色々な箇所を書き変えて改造したり、これから作りたいWebアプリケーションの土台としたり、自由にお使い下さい。

各サンプルコードの概要
----------------------

### usage-blankmap-areapolygon

[白地図レイヤー](http://developer.yahoo.co.jp/webapi/map/openlocalplatform/v1/js/reference/YLayer.html#BlankMapLayer)の使い方を紹介したサンプルコードです。

スタイルを指定することによって、指定のエリアを色分け表示して解りやすく表現することができます。

### usage-blankmap

[白地図レイヤー](http://developer.yahoo.co.jp/webapi/map/openlocalplatform/v1/js/reference/YLayer.html#BlankMapLayer)の使い方を紹介したサンプルコードです。

白地図レイヤーを使うと、市区町村ごとに地図を塗り分けることができます。

### usage-heatmap

[GeoXml切り替えプラグイン](http://developer.yahoo.co.jp/webapi/map/openlocalplatform/v1/js/reference/YPlugin.html#GeoXmlPlugin)の使い方を紹介したサンプルコードです。

GeoXml切り替えプラグインを使うと、[YDF](http://developer.yahoo.co.jp/webapi/map/openlocalplatform/v1/ydf/)でマークアップされた地点情報の集合度を視覚的な情報として地図上に表現できます。

### usage-routesearch

[経路探索プラグイン](http://developer.yahoo.co.jp/webapi/map/openlocalplatform/v1/js/reference/YPlugin.html#RouteSearchPlugin)の使い方を紹介したサンプルコードです。

経路探索プラグインを使うと、指定した地点間の経路探索をインタラクティブUIから指定して行えます。

### usage-stylemap

[スタイル地図レイヤー](http://developer.yahoo.co.jp/webapi/map/openlocalplatform/v1/js/reference/YLayer.html#StyleMapLayer)の使い方を紹介したサンプルコードです。

スタイル地図レイヤーを使うと、地図のベースカラーを変更したり、地図上から道路や建物を消したりといったスタイルを自由に変更できます。

### usage-zipcodesearch

[郵便番号検索API](http://developer.yahoo.co.jp/webapi/map/openlocalplatform/v1/zipcodesearch.html)の使い方を紹介したサンプルコードです。

郵便番号検索APIでは、郵便番号に関する情報を取得できます。
郵便番号を指定して、位置情報（地点名・緯度・経度）を取得できます。

### webapp-animation-weather

[雨雲レーダーレイヤー](http://developer.yahoo.co.jp/webapi/map/openlocalplatform/v1/js/reference/YLayer.html#WeatherMapLayer)の使い方を紹介したサンプルコードです。

雨雲レーダーのアニメーション表示ができます。

### webapp-distribution-mcdonalds

株式会社翔泳社が運営するCodeZineへ寄稿した[YOLP Hacks：API群を組み合わせてオリジナルWebアプリケーションを作る](http://codezine.jp/article/detail/6103)という記事に書かれた、Yahoo! JavaScriptマップAPIを利用して作るWebアプリケーションのサンプルコードです。

東京23区のうち、選択された地点を中心とするショップ情報分布をヒートマップで表示します。

### webapp-measure-distance

株式会社翔泳社が運営するCodeZineへ寄稿した[YOLP Hacks： APIの使い方～現在位置の常時表示／地図をなぞって距離を計測](http://codezine.jp/article/detail/5907)という記事に書かれた、Yahoo! JavaScriptマップAPIを利用して作るWebアプリケーションのサンプルコードです。

地図上のマウスでなぞられた部分に線を引き、その距離を計測できます。

このサンプルコードはGoogle Chromeブラウザに最適化されています。

### webapp-nearby-mcdonalds

株式会社翔泳社が運営するCodeZineへ寄稿した[YOLPで挑戦～「マクドナルドはどこだ」アプリをHTML5で作る！](http://codezine.jp/article/detail/6473)という記事に書かれた、Yahoo! JavaScriptマップAPIを利用して作るWebアプリケーションのサンプルコードです。

現在地から最寄りのマクドナルドまでのルートと店舗の詳細情報を地図上に表示します。

このサンプルコードはiPhone Safariブラウザ、Android標準ブラウザに最適化されています。

### webapp-osc-2012-nagoya

オープンソースカンファレンス2012Nagoya、[YOLP30分クッキング　Yahoo! JAPANのエンジニアがその場で作るスマホ地図サービス](https://www.ospn.jp/osc2012-nagoya/modules/eguide/event.php?eid=36)の中でコーディングした、Yahoo! JavaScriptマップAPIを利用して作るWebアプリケーションのサンプルコードです。

地図上をタップして作成したルートをLatLongLabの[ルートラボconnect](http://latlonglab.yahoo.co.jp/route/connect)から投稿できます。

このサンプルコードはiPhone Safariブラウザ、Android標準ブラウザに最適化されています。

イベント当日の資料は、以下のスライドをご覧下さい。ライブコーディング用の発表資料となりますので、スライドとソースコードを合わせて読み進めることをお薦めします。

* [YOLP 30分クッキング(SlideShare)](http://www.slideshare.net/techblogyahoo/yolp-30)

### webapp-routesearch-weather

株式会社翔泳社が運営するCodeZineへ寄稿した[ルートを探しながら雨雲をチェック！ YOLPで作る簡単便利地図アプリ](http://codezine.jp/article/detail/6837)という記事に書かれた、Yahoo! JavaScriptマップAPIを利用して作るWebアプリケーションのサンプルコードです。

現在地から指定した場所へのルート検索を行いつつ、ルート上の雨雲状況をビジュアルにチェックできるスマホ・タブレット用のWebアプリです。

このサンプルコードはiPhone Safariブラウザ、Android標準ブラウザに最適化されています。


ライセンス
----------

このサンプルコードはMITライセンスにて提供しています。詳しくは [LICENSE](https://github.com/yahoojpYOLP/yolp-jsapi-samples/blob/master/LICENSE) をご確認ください。

サポート
--------

Yahoo! Open Local Platformチームでは、次の場所で開発者サポートを行っています。

* [Yahoo!グループ: Yahoo!地図Web API](http://groups.yahoo.co.jp/group/YJDN-map/)
    * 投稿にはYahoo! JAPAN IDが必要です。
* [@yahoojpYOLP](https://twitter.com/#!/yahoojpYOLP)
    * 投稿にはTwitter IDが必要です。
