# Project gradle：
## google()访问google库获取资源
	repositories {
        	google()
        	jcenter()
   		 }
# App gradle
## retrpfit 封装okhttp网络请求   
	implementation 'com.squareup.retrofit2:retrofit:2.9.0'
## Okhttp 网络请求
	implementation("com.squareup.okhttp3:okhttp:4.7.2")
## Gson 解析json文件
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
 