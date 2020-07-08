# Project gradle：
## google()访问google库获取资源
	repositories {
        	google()
        	jcenter()
   		 }
# App gradle
---
---
## 网络请求
为保证用户数据和设备的安全，Google针对 Android 系统(Android P) 以后的应用程序，将要求默认使用加密连接，Android P 以及之后更新将禁止 App 使用所有未加密的连接，因此运行 Android P 系统以后的安卓设备无论是接收或者发送流量，都不能明码传输，需要使用下一代(Transport Layer Security)传输层安全协议
****
因此在Android P 使用HttpUrlConnection进行http请求会出现以下异常
	W/System.err: java.io.IOException: Cleartext HTTP traffic to **** not permitted
使用OKHttp请求则出现
	java.net.UnknownServiceException: CLEARTEXT communication ** not permitted by network security policy
为解决该问题，在AndroidManifest.xml文件下的application标签增加以下属性
	android:usesCleartextTraffic="true"
##之后
### retrpfit 封装okhttp网络请求   
	implementation 'com.squareup.retrofit2:retrofit:2.9.0'
### Okhttp 网络请求
	implementation("com.squareup.okhttp3:okhttp:4.7.2")
---
---
## Gson 解析json文件
	implementation 'com.google.code.gson:gson:2.8.6'
## Glide 加载网络图片
	implementation 'com.github.bumptech.glide:glide:4.11.0'
	annotationProcessor 'com.github.bumptech.glide:compiler:4.11.0'
## recyclerview布局
	implementation 'com.android.support:recyclerview-v7:28.0.0'
## design库的引用，很多ui控件会用到
	implementation 'com.android.support:design:29.0.3'
## viewbinding的使用（后期会研究databinding）
	android{
	buildFeatures {..
        viewBinding true
    	}
 	..}
 