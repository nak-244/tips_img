### 背景固定画像でスライドショーを実装する

まずは必要なファイルを公式からダウンロードする。

[「Vegas」公式](http://vegas.jaysalvat.com/)

必要なファイルは、ダウンロードしたファイルのうち、下記だけ。

 - vegas.min.css
 - vegas.min.js

上記ファイルを所定の場所にアップロードし、jQuery本体と一緒にプラグインを読み込ませます。
head内に記述すること。

    <link rel="stylesheet" href="css/vegas.min.css">
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.11.0/jquery.min.js"></script>
    <script src="js/vegas.min.js"></script>
次に、必要なスクリプトを記述する。
これもhead内。

    <script>
    $(function(){  
      $('#mainvisual').vegas({ //背景画像でスライドショーしたい場所の設定
      // $('body').vegas({  bodyに直接でもOK
        slides: [
         { src: 'images/mainvisual01.jpg' }, //スライドする画像を配列で設定
         { src: 'images/mainvisual02.jpg' },
         { src: 'images/mainvisual03.jpg' },
        ],
         delay:  5000,  //スライドまでの時間ををミリ秒単位で設定
         timer:  true,  //タイマーバーの表示/非表示を切り替え
         overlay:  'img/01.png',  //オーバーレイする画像の設定
         animation:  'random',  //スライドのアニメーションを設定
         transition:  'blur',  //スライド間のエフェクトを設定
         transitionDuration:  1000  //エフェクト時間をミリ秒単位で設定
         });
         });
     </script>

以上です。

**downloadフォルダにzip保存済み。**
