# 快速开始
使用该项目前，你需要检查你本地的开发环境，避免出现问题
## 所需环境
这里列出项目所需的环境与相关安装教程，方便刚入门的同学
```
1、JDK：1.8+ 
安装教程：https://www.runoob.com/java/java-environment-setup.html
2、Redis 3.0+
安装教程：https://www.runoob.com/redis/redis-install.html
3、Maven 3.0+
安装教程：https://www.runoob.com/maven/maven-setup.html
4、MYSQL 5.5.0+
安装教程：https://www.runoob.com/mysql/mysql-install.html
5、Node v10+
安装教程：https://www.runoob.com/nodejs/nodejs-install-setup.html
```

::: tip
前端安装完 node 后，最好设置下淘宝的镜像源，不建议使用 cnpm（可能会出现奇怪的问题）
:::

```
npm config set registry https://registry.npm.taobao.org
配置后可通过下面方式来验证是否成功
npm config get registry

在 ~/.npmrc 加入下面内容，可以避免安装 node-sass 失败
sass_binary_site=https://npm.taobao.org/mirrors/node-sass/

.npmrc 文件位于
win：C:\Users\[你的账户名称]\.npmrc
linux：直接使用 vi ~/.npmrc
```
## 开发准备
::: tip
在使用该系统前，你还需要做如下准备
:::

1、给 [idea](https://blog.csdn.net/wochunyang/article/details/81736354) 或者 [eclipse](https://blog.csdn.net/magi1201/article/details/85995987) 安装 lombok 插件，我们用它可以省略get，set 方法，可以使代码更简洁，
具体查看 [lombok教程](https://www.ydyno.com/archives/1147.html)

2、了解MapStruct，项目用到了他映射实体，如果你不熟悉可以查看：[熟悉MapStruct](https://www.jianshu.com/p/3f20ca1a93b0)

3、你需要有 Spring boot 的基础，推荐教程 [Spring Boot 2.0 学习](https://github.com/ityouknow/spring-boot-examples)

4、你还需要有 [Vue](https://cn.vuejs.org/v2/guide/) 的基础，推荐入门视屏教程 [网易云课堂](https://study.163.com/course/courseMain.htm?courseId=1004711010)

## 运行项目
::: tip
因为本项目是前后端分离的，所以需要前后端都启动好，才能进行访问
:::

### 后端运行
1、克隆项目：`git clone https://gitee.com/elunez/eladmin.git`

2、导入项目：使用 idea 直接导入项目，安装依赖后，进入 `eladmin-system`模块，执行 `AppRun`

3、导入数据：打开数据库，创建一个新库 `eladmin`，导入sql文件夹中的初始化脚本

![](https://img.el-admin.xin/20200605112835.png)

### 前端运行
1、克隆项目：`git clone https://gitee.com/elunez/eladmin-web.git`

2、安装依赖：打开项目后输入命令安装依赖 `npm install`

3、运行项目：`npm run dev`

启动完后打开 [localhost:8013](localhost:8013) 即可

### 常见问题
*1、依赖安装失败*

可通过配置淘宝的镜像源解决
```
npm config set registry https://registry.npm.taobao.org
配置后可通过下面方式来验证是否成功
npm config get registry

在 ~/.npmrc 加入下面内容，可以避免安装 node-sass 失败
sass_binary_site=https://npm.taobao.org/mirrors/node-sass/

.npmrc 文件位于
win：C:\Users\[你的账户名称]\.npmrc
linux：直接使用 vi ~/.npmrc
```
*2、linux 系统在安装依赖的时候会出现 node-sass 无法安装的问题*

解决方案：
```
1. 单独安装：npm install --unsafe-perm node-sass 
2. 直接使用：npm install --unsafe-perm
```
