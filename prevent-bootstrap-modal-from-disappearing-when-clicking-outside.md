## Prevent Bootstrap Modal from disappearing when clicking outside
* <https://stackoverflow.com/a/54167874/4802664>

```html
<button class='btn btn-danger fa fa-trash' 
data-toggle='modal' 
data-target='#deleteModal' 
data-backdrop='static' 
data-keyboard='false'>
</button>
```
