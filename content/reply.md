# Reply

### url:http://tieba.baidu.com/f/commit/post/add

### method:POST
	
### POST DATA:
```
	ie=utf-8;
	files=[];
	__type__=reply;
	mouse_pwd_isclick=0;
	vcode_md5=;
	kw=剑网3; //贴吧名字  eg: 剑网3
	fid=1185508; //贴吧编号 
	tid=4848846889; //帖子id,  eg：http://tieba.baidu.com/p/4848846889   => 4848846889
	rich_text=1;
	floor_num=0;
	mouse_pwd_t=1478326792; //unix时间戳 eg: 1478326792 ，代表 2016/11/5 14:19:52  
	mouse_pwd= …………………………,14783267920;//unix时间戳的最后加0  ，1478326792 0 =>14783267920，………………部分每个人不同，手动发帖一次在http-header里面自己抓取
	content= 发帖了！！！;//发帖内容
	tbs= c361372910cd57ef1478325339;		//使用getTBS获取 {"tbs":"c361372910cd57ef1478325339","is_login":1} => c361372910cd57ef1478325339
```

每次回复的时候需要更新的内容
```
mouse_pwd_t   //php : time()
mouse_pwd     //php: time()."0"
content
tbs
```



![Formdata](https://github.com/ShanaMaid/baidu-tieba-api/raw/master/content/reply.png)



### return
		
		eg:
		
		{"no":0,"err_code":0,"error":null,"data":{"autoMsg":"","fid":1185508,"fname":"\u5251\u7f513","tid":4847399087,"is_login":1,"content":"\u6211\u5c31\u662f\u4e00\u4e2a\u673a\u5668\u4eba\u800c\u5df2","access_state":null,"vcode":{"need_vcode":0,"str_reason":"","captcha_vcode_str":"","captcha_code_type":0,"userstatevcode":0},"mute_text":null}}
		
		如果"no":0,"err_code":0,发帖成功！
	