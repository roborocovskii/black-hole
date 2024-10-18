# Black Hole Effect (Javascriptでブラックホール風エフェクト)

![Black Hole Effect](images/BlackHoleEffect.jpg)

これは、JavaScriptを使って作成したブラックホールの視覚効果です。

マウスカーソルを、画面の一定の位置で止めていると、そこに周辺から無数の点が集まって来るというものです。

点は大小さまざまでカラフルです。

マウスを動かすと中心(ブラックホール)もマウスに合わせて動きます。

・JavaScriptで描画やアニメーションを行うためにcanvas要素を使います。

・Particleクラスを作り、粒子（点）の初期位置、サイズ、色、速度をランダムに設定します。

・マウスの位置に対して粒子が引き寄せられるようにしマウスを動かすと「ブラックホール」が動きます。

・canvas.getBoundingClientRect()を使用して、キャンバスの画面上の位置を取得し、それを使ってevent.clientXやevent.clientYからオフセットを引くことで、正確なマウス位置を取得しマウス位置のズレを修正します。
・requestAnimationFrameを使ってフレームレートを30fpsに制限し描画頻度を減らし負荷を軽くします。

・ブラックホールから500ピクセル以上離れた粒子は描画をスキップし不要な計算を省略します。

・粒子の色やサイズは初期化時に一度だけ計算し、それを使い回すことで毎フレームの計算を減らします。

・スマートフォンのタッチ動作に対応。

 [デモ先]([https://url.html](https://www.hekeke.com/blog/2024/10/black-hole-effect.html))
