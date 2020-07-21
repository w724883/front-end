### 获取 cookie
```js
function getCookie(cname){
    var name = cname + "=";
    var ca = document.cookie.split(';');
    for(var i=0; i<ca.length; i++) {
        var c = ca[i].trim();
        if (c.indexOf(name)==0) {
            return c.substring(name.length, c.length);
        }
    }
    return "";
}
```

### 修改 cookie
```js
function setCookie(cname, cvalue, exdays) {
  var d = new Date();
  d.setTime(d.getTime() + (exdays*24*60*60*1000));
  var expires = "expires=" + d.toGMTString();
  document.cookie = cname + "=" + cvalue + "; " + expires;
}
```

### 删除 cookie
document.cookie = "username=; expires=Thu, 01 Jan 1970 00:00:00 GMT"; // expires设置为以前的时间

