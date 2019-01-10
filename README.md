# upload

蒲公英 gradle 插件 api v2 版

支持更新日志上传
使用的是自己团队私服 所以没上传公共仓库 没有私服的 可以本地使用 适合独立开发
如果想使用公共库的

查看(代码基本有删减和增加功能改变了 api-v2 和增加了上传更新日志功能)

> Github 地址： dodocat/pgyer
>
> 作者： 荆全齐
>
> 功能介绍： 使用 gradle 上传 app 到蒲公英。
>
> https://github.com/dodocat/pgyer

> 蒲公英 api 文档
> https://www.pgyer.com/doc/view/api#paramInfo

```
buildscript {

    repositories {
        maven { url 'http://' }
    }

    dependencies {
        classpath 'com.android.tools.build:gradle:3.2.1'

        classpath 'com.pgyer.upload:plugins:0.1.0'
    }
}

apply plugin: 'pgyerUpload'

pgyer {
    _api_key = "蒲公英申请的key"
    desc = new String("${project.UPDATE_DESCRIPTION}")
}

apks {
    release {
        sourceFile = file("./abc.apk")
    }
}

gradle.properties

UPDATE_DESCRIPTION = "ceshi"
```

> 使用
>
> Gradle app--> pgyer --> uploadPgyer
