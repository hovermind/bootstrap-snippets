## JS
```js
"use strict";

function isFormInputValid() {
  
  let isValid = true;
  
  //validation logic here
  
  let sid = $('#sid');
  if (!sid.val()) {
    isValid = false;
  }
  
  return isValid;
}

function hasWarning() {
  
  let hasWarning = false;
  
  // warning logic here
  
  let sid = $('#sid');
  if(sid.val() === '****'){
    hasWarning = true;
  }
  
  return hasWarning;
}

function setAlertModalHeaderColor(alerType){
  
  let headerClass = 'modal-header modal-header-default';
  
  if(alerType === 'warning'){
    headerClass = 'modal-header modal-header-warning';
  }
  
  if(alerType === 'error'){
    headerClass = 'modal-header modal-header-danger';
  }
  
  let $modalHeader = $("#alert-modal-header");
  
  $modalHeader.removeClass();
  
  $modalHeader.addClass(headerClass);
}

function showAlert(alerType, title, body, callback) {
  
  if(!alerType){
    alerType = "warning";
  }
  
  setAlertModalHeaderColor(alerType);
  
  if(!title){
    title = "Warning!";
  }
  
  if(!body){
    body = "this is a warning"; 
  }
  
  $('#alert-modal-title').html(title);
  $('#alert-modal-body').html(body);

  let $alert = $('#alert-modal');
  // remove previous event listener
  $alert.off('hidden.bs.modal');
  // add event listener
  $alert.on('hidden.bs.modal', callback);
  // show alert
  $alert.modal('show');
}

function registerAlertDialog(){
  
    $('form').on('submit', function(e) {
    
    /*
     * return 「false」 => e.preventDefault()
     * return 「true」 => Form submit
     */
    
    //console.log("On Submit");
    let $form = $(this)[0];
    
    // Input check
    let allInputOk = isFormInputValid();
    let warning = hasWarning();
    
    if (allInputOk) {
      
      console.log("allInputOk");
      
      if (warning) { //show warning modal
        
        console.log("warning");
        
        showAlert('warning', "", "", function(e) { // default
          
          //console.log("Warning Modal is closed");

          $form.submit();
          
        });
        
      }
      
    } else { // sho error modal
      
      //console.log("Input invalid");
      
      showAlert('error', "Error!", "This is an error message", function(e) {
        
        //console.log("Error Modal is closed");
        
      });
      
    }
    
    return (allInputOk && !warning);
  });
  
}

$(function() {
  
  
  registerAlertDialog();

});
```
## CSS
**don't forget to put css in the head section**
```css
/* CSS used here will be applied after bootstrap.css */
.modal-header-success {
    color:#fff;
    padding:9px 15px;
    border-bottom:1px solid #eee;
    background-color: #5cb85c;
    -webkit-border-top-left-radius: 5px;
    -webkit-border-top-right-radius: 5px;
    -moz-border-radius-topleft: 5px;
    -moz-border-radius-topright: 5px;
     border-top-left-radius: 5px;
     border-top-right-radius: 5px;
}
.modal-header-warning {
	color:#fff;
    padding:9px 15px;
    border-bottom:1px solid #eee;
    background-color: #f0ad4e;
    -webkit-border-top-left-radius: 5px;
    -webkit-border-top-right-radius: 5px;
    -moz-border-radius-topleft: 5px;
    -moz-border-radius-topright: 5px;
     border-top-left-radius: 5px;
     border-top-right-radius: 5px;
}
.modal-header-danger {
	color:#fff;
    padding:9px 15px;
    border-bottom:1px solid #eee;
    background-color: #d9534f;
    -webkit-border-top-left-radius: 5px;
    -webkit-border-top-right-radius: 5px;
    -moz-border-radius-topleft: 5px;
    -moz-border-radius-topright: 5px;
     border-top-left-radius: 5px;
     border-top-right-radius: 5px;
}
.modal-header-info {
    color:#fff;
    padding:9px 15px;
    border-bottom:1px solid #eee;
    background-color: #5bc0de;
    -webkit-border-top-left-radius: 5px;
    -webkit-border-top-right-radius: 5px;
    -moz-border-radius-topleft: 5px;
    -moz-border-radius-topright: 5px;
     border-top-left-radius: 5px;
     border-top-right-radius: 5px;
}
.modal-header-primary {
	color:#fff;
    padding:9px 15px;
    border-bottom:1px solid #eee;
    background-color: #428bca;
    -webkit-border-top-left-radius: 5px;
    -webkit-border-top-right-radius: 5px;
    -moz-border-radius-topleft: 5px;
    -moz-border-radius-topright: 5px;
     border-top-left-radius: 5px;
     border-top-right-radius: 5px;
}
```

## Sample hmtl
```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width">
  <title>Foo Word Check</title>
  <link href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.6/css/bootstrap.min.css" rel="stylesheet" type="text/css" />
</head>
<body>
  
  <form action="/" method="POST">
    <input id="sid" name="sid" type="text" placeholder=" SID" />
    <input type="submit" value="Send" />
  </form>
  
  
<div id="alert-modal" class="modal fade">
  <div class="modal-dialog">
    <div class="modal-content">
      <div id="alert-modal-header" class="modal-header modal-header-danger">
        <button type="button" class="close" data-dismiss="modal" aria-label="Close"><span aria-hidden="true">&times;</span></button>
        <h4 id="alert-modal-title" class="modal-title"></h4>
      </div>
      <div id="alert-modal-body" class="modal-body"></div>
      <div class="modal-footer">
        <button type="button" class="btn btn-default" data-dismiss="modal">Ok</button>
      </div>
    </div>
  </div>
</div>
  
<script src="https://code.jquery.com/jquery.min.js"></script>
<script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.6/js/bootstrap.min.js"></script>
  
</body>
</html>
```

**Courtesy**
* CSS: https://www.bootply.com/s6x5oKLiDG
* Modal: https://gist.github.com/billmei/2e9d11ff732b1ea6916f
