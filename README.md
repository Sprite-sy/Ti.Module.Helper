一个杂七杂八的ti android module.
================

###主要实现了 
1 百度定位库的包装
2 一些android下内存相关函数
 如gc, 内存占用情况, 手动释放ti的图片cache
 

###使用
	1 百度定位
		var helper = require("com.sprite.helper");
		var r = helper.getBDLocation( function(location) {
			if (location.err != "ok" || !location.locType) {
				//fail here
				return;
			}
			console.log(location);
			return;
		}, {
			openGps: true
		}); 
		
	2 其它
		helper.freeImageCache();
		helper.systemGc();
