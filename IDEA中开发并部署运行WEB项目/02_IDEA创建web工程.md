> 推荐先创建一个空项目，这样可以在一个空项目下同时存在多个 modules，不用后续来回切换之前的项目，当然也可以忽略此步直接创建 `web` 项目

<img src="images/1681458194939.png" alt="1681458194939" style="zoom: 60%;" />

<img src="images/1681458273381.png" alt="1681458273381" style="zoom: 60%;" />

> 检查项目的 SDK、语法版本、以及项目编译后的输出目录

<img src="images/1681458343921.png" alt="1681458343921" style="zoom:50%;" />

<img src="images/1681458393871.png" alt="1681458393871" style="zoom: 55%;" />

> 先创建一个普通的 JAVA 项目

<img src="images/1681458485837.png" alt="1681458485837" style="zoom:63%;" />

> 检查各项信息是否填写有误

<img src="images/1681458599545.png" alt="1681458599545" style="zoom:60%;" />

> 创建完毕后，为项目添加 Tomcat 依赖

<img src="images/1681458857830.png" alt="1681458857830" style="zoom: 67%;" />

<img src="images/1681458897017.png" alt="1681458897017" style="zoom: 95%;" />

<img src="images/1681458939400.png" alt="1681458939400" style="zoom:70%;" />

> 选择 modules，添加 framework support（如果找不到使用记得全局搜索（快捷键 `ShiftShift`）（记得先选中模块））

<img src="images/1681458672258.png" alt="1681458672258" style="zoom: 80%;" />

> 选择 Web Application 注意 Version 为 5.0（如果上面没有为项目添加 Tomcat10 依赖的话是选不了的（新版已经是6.0了）），勾选  Create web.xml

<img src="images/1681459007273.png" alt="1681459007273" style="zoom:80%;" />

> 删除 index.jsp，替换为 index.html

![1681459080873](images/1681459080873.png)

<img src="images/1681459147133.png" alt="1681459147133" style="zoom: 67%;" />

### 处理配置文件

+ 在工程下创建 `resources` 目录，专门用于存放配置文件(都放在`src`下也行，单独存放可以尽量避免文件集中存放造成的混乱)
+ 标记目录为资源目录，不标记的话则该目录不参与编译

<img src="images/1681461443278.png" alt="1681461443278" style="zoom:67%;" />

+ 标记完成后,显示效果如下

<img src="images/1681461513406.png" alt="1681461513406"  />

### 处理依赖jar包问题
+ 在 `WEB-INF` 下创建 `lib`目录
+ 必须在 `WEB-INF` 下，且目录名必须叫 `lib` !!!
+ 复制 jar文件进入 `lib` 目录

![1681461788411](images/1681461788411.png)

+ 将lib目录添加为当前项目的依赖，后续可以用maven统一解决

<img src="images/1681461846178.png" alt="1681461846178" style="zoom:67%;" />

![1681461881121](images/1681461881121.png)

+ 环境级别推荐选择module 级别，降低对其他项目的影响，name可以空着不写

![1681461923761](images/1681461923761.png)

### 查看当前项目有那些环境依赖

![1681463867295](images/1681463867295.png)

<img src="images/1681462179671.png" alt="1681462179671" style="zoom:50%;" />

+ 在此位置，可以通过-号解除依赖

<img src="images/1681462247973.png" alt="1681462247973" style="zoom:85%;" />