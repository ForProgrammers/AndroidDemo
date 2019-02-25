

### 项目的一些配置

gradle.properties 中配置 一些版本信息

 * android版本
 * kotlin 版本
 * 三方库版本
 * app版本
 
创建子项目后在其build.gradle 中添加

```
def isLib = true

if (isLib) {
    apply from: rootProject.apply_as_lib
} else {
    apply from: rootProject.apply_as_app
}

```

> 创建的子项目中 在 /src/main 文件夹下面 创建两个目录  /app 和/lib 分别放对应的Manifest文件

 
如果想在项目中配置一些公共参数 可以在 /config/project_ext.gradle 中配置 调用的时候 直接rootProject.调用
