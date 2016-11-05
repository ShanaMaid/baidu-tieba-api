#cookie

在访问百度的时候应该带上登录状态的cookie

你可以在http-header中找到你的cookie
 


cookie应该带有以下字段

```
 BAIDUID 
 TIEBA_USERTYPE
 BDUSS
 TIEBAUID 
 bdshare_firstime
 rpln_guide
 wise_device
```

如下图所示：
获取cookie

 chrome -> F12 -> network -> type = xhr

 ![cookie](https://github.com/ShanaMaid/baidu-tieba-api/raw/master/content/cookie.png)