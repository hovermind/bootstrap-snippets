## Bootstarp Toast
```html
<div id="setting-toast" class="toast ml-auto" role="alert" data-delay="10000" data-autohide="true">
  <div class="toast-header bg-primary">
    <strong id="setting-toast-title" class="mr-auto text-white">設定保存</strong>
    <button type="button" class="ml-2 mb-1 close" data-dismiss="toast" aria-label="Close">
      <span aria-hidden="true" class="text-white">×</span>
    </button>
  </div>
  <div id="setting-toast-body" class="toast-body">設定を保存しました。</div>
</div>
```

## JS
```js
function showSettingToast(title, body, delay){

  if(title){
    $('#setting-toast-title').html(title);
  }

  if(body){
     $('#setting-toast-body').html(body);
  }

  let $settingToast = $('#setting-toast');
  if(delay >= 1000){
    $settingToast.data('delay', delay);
  }

  $settingToast.toast('show');
}
```

## Sample
```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width">
  <title>JS Bin</title>
<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.2.1/css/bootstrap.min.css" integrity="sha384-GJzZqFGwb1QTTN6wy59ffF1BuGJpLSa9DkKMp0DgiMDm4iYMj70gZWKYbI706tWS" crossorigin="anonymous">
</head>
<body>
  
  <div id="setting-toast" class="toast ml-auto" role="alert" data-delay="10000" data-autohide="true">
    <div class="toast-header bg-primary">
      <strong id="setting-toast-title" class="mr-auto text-white">設定保存</strong>
      <button type="button" class="ml-2 mb-1 close" data-dismiss="toast" aria-label="Close">
        <span aria-hidden="true" class="text-white">×</span>
      </button>
    </div>
    <div id="setting-toast-body" class="toast-body">設定を保存しました。</div>
  </div>
  
<script src="https://code.jquery.com/jquery-3.2.1.slim.min.js" integrity="sha384-KJ3o2DKtIkvYIK3UENzmM7KCkRr/rE9/Qpg6aAZGJwFDMVNA/GpGFF93hXpG5KkN" crossorigin="anonymous"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.12.9/umd/popper.min.js" integrity="sha384-ApNbgh9B+Y1QKtv3Rn7W3mgPxhU9K/ScQsAP7hUibX39j7fakFPskvXusvfa0b4Q" crossorigin="anonymous"></script>
<script src="https://stackpath.bootstrapcdn.com/bootstrap/4.2.1/js/bootstrap.min.js" integrity="sha384-B0UglyR+jN6CkvvICOB2joaf5I4l3gm9GU6Hc1og6Ls7i6U/mkkaduKaBhlAXv9k" crossorigin="anonymous"></script>
 <script> 
   
  function showSettingToast(title, body, delay){
    
    if(title){
      $('#setting-toast-title').html(title);
    }
    
    if(body){
       $('#setting-toast-body').html(body);
    }
    
    let $settingToast = $('#setting-toast');
    if(delay >= 1000){
      $settingToast.data('delay', delay);
    }
    
    $settingToast.toast('show');
  }
   
  $(function(){
    showSettingToast("設定", "設定を保存しました。", 2000);
  });

 </script>
  
</body>
</html>
```
