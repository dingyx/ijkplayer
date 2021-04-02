# Android ijkplayer

基于Bilibili开源项目 [ijkplayer](https://github.com/bilibili/ijkplayer) 在Ubuntu环境下编译生成的 Android 平台可运行的库。格式支持基本采用default配置，支持主流音视频播放。arm64-v8a、armeabi、armeabi-v7a平台的so大小分别约5~6m

依赖该库后，可参考 [官方使用Demo](https://github.com/bilibili/ijkplayer/tree/master/android/ijkplayer/ijkplayer-example) 编写相应界面即可实现视频播放



* 使用方法

  1. 在项目工程的 build.gradle 中，指定 maven 仓库地址：

   ```groovy

   allprojects {
       repositories {
           google()
           jcenter()
           maven{
               url "https://raw.githubusercontent.com/dingyx/ijkplayer/main"
           }
       }
   }
   ```

     > 主要是指定该仓库地址： “https://raw.githubusercontent.com/dingyx/ijkplayer/main“

  2.  在需要使用该库的 module 下 build.gradle 中添加依赖

   ```groovy
   dependencies {
       implementation fileTree(include: ['*.jar'], dir: 'libs')
       implementation 'androidx.appcompat:appcompat:1.0.0'
       implementation 'com.sdtv.haikan:ijkplayer:0.0.2'
   }
   ```

     > 主要是指定该依赖：'com.sdtv.haikan:ijkplayer:0.0.2'



* 0.0.1 版本，编译了支持 arm64-v8a、armeabi、armeabi-v7a、x86、x86_64 平台 so

* 0.0.2 版本，去掉 x86、x86_64 平台 so



