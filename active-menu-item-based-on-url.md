[Original Article](https://www.infoworld.com/article/3304440/application-development/setting-an-active-menu-item-based-on-the-current-url-with-jquery.html)
```
$(function () {
    setNavigation();
});

function setNavigation() {
    var path = window.location.pathname;
    path = path.replace(/\/$/, "");
    path = decodeURIComponent(path);

    $(".nav a").each(function () {
        var href = $(this).attr('href');
        if (path.substring(0, href.length) === href) {
            $(this).closest('li').addClass('active');
        }
    });
}
```

