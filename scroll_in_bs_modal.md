## CSS
```css
.modal-dialog{
    overflow-y: initial !important;
}
.modal-body{
  height: 250px;
  overflow-y: auto;
}
```

## JS
```js
$(document ).ready(function() {

  console.log("doc. is ready...");

  $('.modal-body').scroll(function(e){

    console.log("modal scrolling is working...");

  });

});
```

## Test Code
* download jQuery (rename as `jquery.js`) and BootStrap and place in the same folder 
* use script and link tag:
```html
// in head
<link rel="stylesheet" type="text/css" href="bootstrap.css">
<style>

</style>

// in bottom
<script src="jquery.js" type="text/javascript"></script>
<script src="bootstrap.bundle.js" type="text/javascript"></script>
<script type="text/javascript">

</script>
```

`scroll-fix.html`
```html
<!DOCTYPE html>
<!--[if lte IE 6]><html class="preIE7 preIE8 preIE9"><![endif]-->
<!--[if IE 7]><html class="preIE8 preIE9"><![endif]-->
<!--[if IE 8]><html class="preIE9"><![endif]-->
<!--[if gte IE 9]><!--><html><!--<![endif]-->
<head>
<meta charset="UTF-8">
<meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1">
<meta name="viewport" content="width=device-width,initial-scale=1">
<title>Scroll fix</title>
<meta name="author" content="name">
<meta name="description" content="description here">
<meta name="keywords" content="keywords,here">
<link rel="stylesheet" type="text/css" href="bootstrap.css">
<style>
	.modal-dialog{
		  overflow-y: initial !important;
	}
	.modal-body{
	  height: 250px;
	  overflow-y: auto;
	}
</style>
</head>
<body>

	<div class="modal fade" id="my-modal" tabindex="-1" role="dialog" aria-labelledby="" aria-hidden="true">
		<div class="modal-dialog" role="document modal-content" style="overflow-y: scroll; max-height:85%;  margin-top: 50px; margin-bottom:50px;">
			<div class="modal-content">
				<div class="modal-header">

					<div style='text-align: right; float: right'>
						<button type="button" class="close" data-dismiss="modal" aria-label="Close">&times;</button>
					</div>

					<h2 class="modal-title">
						<strong>My Modal Title</strong>
					</h2>

				</div>

				<div class="modal-body">
					<div class="panel panel-default">
						<div class="panel-body">

							<div role="alert" class="alert alert-danger">
								<strong>Warning!</strong>
								 Japanese Lorem Ipsum
							</div>
							
							<div>
								<p>
									校のら県惑り苗属年こけ室間ヤタ年格ゃト切7権カヱケ北陽てゃ士工とび宅察ハヘ囲間スヨニマ談品さちわひ市幅クメレタ碁闘トべづ式産朝4認オ光軽ヘタニ名智湾緩どぱよゃ。前そッい介2後ほけび和戦ぼれろ橋提シリタ症価かさラぞ減象ワソユ前井無ムリネフ渕49那おけ拠共ぜのッ者京ね頼氷表ナイワ分無暮にだれか出界終みぽ大堪薫酷くへゃら。

									8延ケイテシ的管ムラカ迎7治ねざ分4待ぎうほ記稿害タネシア朝爆でつま緑情ゆ進郎ナタホシ両塚マモ医今みにけど豊規ろもう遊能ぱよひ主影よゅわ性予ユ渉給頭ぱ時配投妹ごつ。行然がこむ牧奏ろふ紘年づ月特顔マ際全ミ館会9東タヌア業委レ能員おぱぞ設同ウ央豊ユ都64平ルか情聞当ロヱ戸属やこれけ意米卓捨縦ぽイや。

									護リじ真込立ぐこち太稔ゃ退王テヨセキ戸育り配同押つ分載スゃ欲家んづくの記決ゃ六6無リて情排撲隣ぼず。予レセオ型探ミメホ市19食ヲニ海経検に学中ヤユ徴点ぱさだょ見辺セ女宅だ家維政ミユメ籍掲ゅ水題レコエ野冬密宝剛たをンぜ。女近促ゆごょ支落ルノヘチ済89念ノ字健イコリ経競むだしは回経リふ断負ツハヨヲ潟12約ねリぼぶ竹八ノレ町陣メヱヲヨ転場フ段来6昇若夜交やレれっ。

									週括けみ合固ル金変諸読こ際整スシキネ者表ロイタメ旅載り時際フマレ遅訃ょもラ応60衣目とぞみ研稿げ旧略民劣ごがっ。31頼終伴0説すし緊竹テヘ胞校みフむト禁京ノ着争がうぎせ心1出クれがと会抗状ラべ通様園ぱ潟更サチキ著秋スツ池長レこはぐ長療そ重会味運抱てさひ。事庭ワネ器本ゅ違介フレ写購ウロタ型剤原テコ画木民ロ記林レ賞面めきこ回無マスニ応2市ルテチ方化ーちごで代叙孟るゃん。

									員換へ健嘉題っなせた人念しまか込分セケク新買コシホマ考今しへ東3禁げべょ楽目勝ドふ決挙うよれを。歴み向選わイ初自トヌ告画ふはれ香住のぎ切良ンなど査装コフヌ里離ク隣朝イニム質著クヲ注教エモ読面レへぽせ惑通ソトセリ別横練気傍やルかは。部たさづそ夜望ウカヘ止樹ネタ去57機ソチ音9任チラロソ聞38無っば介26寒いん米賀ヱアケ断王群うれ。

									84新カ安際るリーよ亡受ざ原氏ど座滋ご要樹がへぽ仰福みい報岡ーしび努崎始ソチ何1掲ッ愛偶凝ゆ。3害窓整ネワ入曲せ題聞ユ全力めす完権毎アヌハ合採ウ座面自ユマ第倒くぎ容満おへ掲実重運おめ。服天ホ申63短イ東鈴徳ヘノ国他シ変成り断光写っめん弓応アルロレ揺速こフ記来局ニケレナ日89韓め急院ウ乗文ふきせぴ究年ラぜぽ本組キワイル晴性議傾けるざ。

									場ん豆評タイ取通退い同準シ際新イくりせ満時ゅもりし皇必を将責さ能屋間モ題7更わざみぼ議放リ市疾ソテレエ心間ぞじ社提きちたさ。首む比96一しッせ掲周禁個で続問ロ揮拓マ更級びが文断ケホキテ尾注みぽな対力フ神純ヲケトソ表団モト聞42表教ぞぐらむ。体ふー式初タコヘ呼庁トレノ放8投う動改球もめ携連ウオソク際夜柱糖マチヲコ職紀け実舵込庭栃仙け。

									演ワ質難新ソラヨヘ目広強せンゆお意木たがいそ地告セチウヒ身中ま信帳ほスろ以1先げとち浜議談家ッおべぽ。帯ぽわ郵嬬ラ科本ょば元立25増ぜもほ図失ツシ生着きんて字7味カスワホ好問ぶ最来握ヒナミ業頼今ねけひぐ。提ちク録理セウマネ転父かク純辞フる食方写フホ特図ル大別ト市航とぼほあ話係でスひよ稿齢ネ勝欄ょす権大ハネニオ州37廃3静ヤマタ定覇吾んトはや。

									紙シミクム椅野すトか変右むラっげ見現シ送夕サ型提時ず者玲キ苦金満してばト記新なょま鮮真ソト稿築ノ公掲お子身ウモニメ影界ス討4排づ。囲ソ並6表道4道議はス後王ロミユセ臨更識もきこは豆9携ケメス撤来見ニオエ金貨カエニミ家車て美進すぴま本経せもざル数屈裂黙け。

									越ょ著軍ユフ目原ぱ第郵レーくゆ載温ヌラ棋制や田業メレツロ修9講イヤスニ地石す下文メソ現読む枠堺へえ覧政ヌセレソ制覧ぞスきこ人無理ヌソワク歓応更トず。新サテ面型か失択ロネ並機ら断唐えへび斉祝ヨホ際全エヲアラ稿属とをに母千地ぐも置緒激集ゃぞで架弾コ界件記がらぞイ然47全ネ済旅だぜで。
								</p>
							</div>

							<div class="form-group">

								<label class="control-label">User Id</label>
								<input id="user-id" name="user-id" type="number" placeholder="Enter Id" class="form-control">

							</div>
							
							<div class="form-group">

								<label class="control-label">User Name</label>
								<input id="user-name" name="user-name" type="text" placeholder="Enter User Name" class="form-control" />

							</div>
							
							<div class="form-group">

								<label class="control-label">Gender</label>
								<select id="gender-select" name="gender-select" class="form-control">
									<option value="m" text="Male"></option>
									<option value="f" text="Female"></option>
								</select>

							</div>

							<!--/* feedback message to user */-->
							<div role="alert" class="alert feedback-success alert-dismissable" id="feedback_div">
								<div style='text-align: left'>
									<div style='text-align: right; float: right'>
										<button data-dismiss="alert" class='close alert-close' aria-label="close" aria-hidden='true' tabindex='-1'>&times;</button>
									</div>
									<strong id="feedback_message">Feedback Message</strong>
								</div>
							</div>

							<div class="form-group" style="float: right;">
								<button type="button" class="btn btn-success" id="btn-creat-user">Create</button>
								<button type="button" class="btn btn-danger" data-dismiss="modal" id="btn-close">Close</button>
							</div>
						</div>
					</div>
				</div>
			</div>
		</div>
	</div>
	
	<button id="btn-my-modal" type="button" class="btn btn-success" data-toggle="modal" data-target="#my-modal">Create User</button>

	<script src="jquery.js" type="text/javascript"></script>
	<script src="bootstrap.bundle.js" type="text/javascript"></script>
	<script type="text/javascript">

  
	$(document ).ready(function() {
		
		console.log("doc. is ready...");
		
		$('.modal-body').scroll(function(e){
		
			console.log("modal scrolling is working...");
			
		});

	});
	
  </script>
</body>
</html>
```
