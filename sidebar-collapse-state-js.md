## Retainning Sidebar Open/Close State
BaseViewModel & MyViewModel
```
public class BaseViewModel {

	private String menuStateFlag = "1";

	public String getMenuStateFlag() {
		return menuStateFlag;
	}

	public void setMenuStateFlag(String menuStateFlag) {
		this.menuStateFlag = menuStateFlag;
	}
}

public class ConfigViewModel extends BaseViewModel { 

	// ... ... ... ...
}
```

Hidden field in `master.html` (thymeleaf template) with id `id="menuStateFlag"`
```
<input type="hidden" id="menuStateFlag" th:field="*{menuStateFlag}" />
```

`sidebar.js`
```
function isMenuOpen() {
	return !($("#wrapper").hasClass('toggled'));
}

function setMenuStateFlag(flag) {
	$('#menuStateFlag').val(flag);
}

function toggleState() {
	
	let $indicatorArrow = $('#arrow_icon');
	
	if (isMenuOpen()) {

		$indicatorArrow.toggleClass("fa-chevron-left fa-chevron-right");
		setMenuStateFlag(0);

	} else {

		$indicatorArrow.toggleClass("fa-chevron-right fa-chevron-left")
		setMenuStateFlag(1);
	}

	$("#wrapper").toggleClass("toggled");
}

$(document).ready((e) => {

	$("#menu-toggle").click(function(e) {
		e.preventDefault();
		toggleState();
	});
	
	/*
	* retain menu state 
	* $('#menuStateFlag').val() => flag val from hidden field with id '#menuStateFlag'
	* hidden field is bind to flag property of ViewModel => ViewModelinherited from BaseViewModel
	*/
	if( $('#menuStateFlag').val() == 0 && !$("#wrapper").hasClass('toggled') ){ // hasClass('toggled') == true => means closed
	    $("#wrapper").setClass('toggled')
	}
});
```
