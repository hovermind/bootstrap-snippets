## JS for Toogle of Collapsible Sidebar
`sidebar.js`
```
function isMenuOpen() {
	return !($("#wrapper").hasClass('toggled'));
}

function toggleState() {
	
	let $indicatorArrow = $('#arrow_icon');
	
	if (isMenuOpen()) {

		$indicatorArrow.toggleClass("fa-chevron-left fa-chevron-right");

	} else {

		$indicatorArrow.toggleClass("fa-chevron-right fa-chevron-left")
	}

	$("#wrapper").toggleClass("toggled");
}

$(document).ready((e) => {

	$("#menu-toggle").click(function(e) {
		e.preventDefault();
		toggleState();
	});
});
```

See: [Retaining Sidebar Open/Close STate](https://github.com/hovermind/bootstrap-snippets/blob/master/sidebar-collapse-state-js.md)
