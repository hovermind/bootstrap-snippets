## Collapsible Sidebar with Fixed Top Navigation
Required:
* [jQuery](#)
* [Bootstarp](#)
* [font-awesome](#)
* [`sidebar.css`](https://github.com/hovermind/bootstrap-snippets/blob/master/sidebar-css.md)
* [`sidebar.js`](https://github.com/hovermind/bootstrap-snippets/blob/master/sidebar-js.md)

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

## `sidebar-fixed-top.html`
```
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">

<title>Fixed Top with Collapsible Sidebar</title>

<link rel="stylesheet" href="css/bootstrap.css" />
<link rel="stylesheet" href="css/font-awesome/css/font-awesome.css" />
<link rel="stylesheet" href="css/page.css" />
<link rel="stylesheet" href="css/top-bar.css" />
<link rel="stylesheet" href="css/sidebar.css" />

<script type="text/javascript" src="js/jquery.js"></script>
<script type="text/javascript" src="js/bootstrap.js"></script>
<script type="text/javascript" src="js/sidebar.js"></script>

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
	
			<div id="wrapper">

				<div id="sidebar-wrapper">

					<ul class="sidebar-nav" style="margin: 0;">

						<li class="sidebar-brand">
							<a href="#menu-toggle" id="menu-toggle" style="margin-top: 20px; float: right;">
								<i id="arrow_icon" class="fa fa-chevron-left" style="font-size: 20px !Important;" aria-hidden="true"></i>
							</a>
						</li>

						<li>
							<a href="#" >
								<span style="margin-left: 90px;">Menu 1</span>
							</a>
						</li>
						
						<li>
							<a href="#" >
								<span style="margin-left: 90px;">Manu 2</span>
							</a>
						</li>
						
					</ul>

				</div>


				<div id="page_content" >
				
					<div  class="container" style="padding-top: 10px;">
					
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
					
				</div>
        </div>
	</div>

</body>
</html>
```
