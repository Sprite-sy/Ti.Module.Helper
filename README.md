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
		
		需要修改 请参考http://developer.baidu.com/map/geosdk-android-developv3.3.htm#.E8.AE.BE.E7.BD.AEAndroidManifest.xml


	2 其它
		helper.freeImageCache();
		helper.systemGc();

###其它 
	1.[设置AndroidManifest.xml](http://developer.baidu.com/map/geosdk-android-developv3.3.htm#.E8.AE.BE.E7.BD.AEAndroidManifest.xml)<br />  
