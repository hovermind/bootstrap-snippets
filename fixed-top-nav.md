## Fixed Top Navigation
Required:
* [jQuery](#)
* [Bootstarp](#)
* [font-awesome](#)

`page.css`
```
body{
	margin: 0px;
	padding-top: 50px;
}
```

`top-bar.css`
```
#top_bar{
	font-family: meiryo;
	font-size: 25px;
	margin: 0px;
	padding: 10px;
}
```

## `fixed-top.html`
```
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">

<title>Fixed Top</title>

<link rel="stylesheet" href="css/bootstrap.css" />
<link rel="stylesheet" href="css/font-awesome/css/font-awesome.css" />
<link rel="stylesheet" href="css/page.css" />
<link rel="stylesheet" href="css/top-bar.css" />

<script type="text/javascript" src="js/jquery.js"></script>
<script type="text/javascript" src="js/bootstrap.js"></script>

</head>

<body>

	<nav id="top_bar" class="navbar navbar-inverse navbar-fixed-top" role="navigation">
		<div class="container">

			<a href="#">Hovermind</a>

			<span style="float: right">
				<a href="#" class="btn btn-info" >Facebook</a>
				<a href="#" class="btn btn-success" >Twitter</a>
				<a href="#" class="btn btn-danger" >Github</a>
			</span>

		</div>
	</nav>

	<div class="container">
	
		<h1>The quick brown fox jumped over the lazy dog</h1>
		<h1>The quick brown fox jumped over the lazy dog</h1>
		<h1>The quick brown fox jumped over the lazy dog</h1>
		<h1>The quick brown fox jumped over the lazy dog</h1>
		<h1>The quick brown fox jumped over the lazy dog</h1>
		<h1>The quick brown fox jumped over the lazy dog</h1>
		
		<h1>The quick brown fox jumped over the lazy dog</h1>
		<h1>The quick brown fox jumped over the lazy dog</h1>
		<h1>The quick brown fox jumped over the lazy dog</h1>
		<h1>The quick brown fox jumped over the lazy dog</h1>
		<h1>The quick brown fox jumped over the lazy dog</h1>
		<h1>The quick brown fox jumped over the lazy dog</h1>
		
		<h1>The quick brown fox jumped over the lazy dog</h1>
		<h1>The quick brown fox jumped over the lazy dog</h1>
		<h1>The quick brown fox jumped over the lazy dog</h1>
		<h1>The quick brown fox jumped over the lazy dog</h1>
		<h1>The quick brown fox jumped over the lazy dog</h1>
		<h1>The quick brown fox jumped over the lazy dog</h1>
		
		<h1>The quick brown fox jumped over the lazy dog</h1>
		<h1>The quick brown fox jumped over the lazy dog</h1>
		<h1>The quick brown fox jumped over the lazy dog</h1>
		<h1>The quick brown fox jumped over the lazy dog</h1>
		<h1>The quick brown fox jumped over the lazy dog</h1>
		<h1>The quick brown fox jumped over the lazy dog</h1>

	</div>

</body>
</html>
```
