# 项目简介
1）代码生成主要依赖于freeMark模板，不同的项目需求可以通过修改freeMark模板来实现。

2）如果是后台管理系统，则可以生成管理系统基本的网站页面及其功能。其他系统则很难生成前端页面，主要困难在于模板不统一，如果页面风格都相似，也可以用模板生成页面，然后再对页面进行修改。

3）项目基本功能：根据数据库表生成基本功能代码，包含Mybatis文件，dao、servic、entity、controller以及查询页面、增加编辑页面。

4)生成过程中可以选择编辑页面所需要的字段，列表页面所需要的字段以及查询条件所需要的字段。
# 数据库
1）数据库文件在项目根目录下的doc文件夹下xcode.sql文件

2）创建数据库xCode 默认设置root账户、密码root123

3）执行xcode.sql文件的SQL，创建数据表结构即可
4）如果数据库名不是xCode，记得修改resources/mapping/GenDataBaseDictDao.xml 下的 getTableList
# 项目结构
1）项目根目录下的doc文件夹放置的是开发相关的文档

2） pom.xml 文件是maven相关配置文件

3）src.main 包下有三个文件夹，Java文件夹很明显，是Java文件相关。   resources文件夹是  配置相关的文件夹，包括spring相关配置，Mybatis相关配置，数据库相关配置，redis相关配     置都在此文件夹下，webapp文件夹下是页面相关的

4）com.cn.cooxin包，admin包主要是管理代码生成后台功能的文件，包含用户的管理、角色菜单管理，代码生成管理等，code包主要是代码生成相关的功能，common包是公共服务相关的功能，ueditor是百度编辑器相关的功能，如果不用，可以不用管。util包是开发工具类相关的功能。
  
# 项目访问
1）导入数据库，配置好项目即可启动。默认访问地址：http://localhost:8080/xCode/admin/ 登陆账户：199199688@qq.com 密码 abc123

2）登陆之后，进入后台系统，左侧两个菜单：基础管理 这个菜单主要是基础功能，代码管理 此菜单是我们需要生成代码主要的功能点，其中数据表管理负责数据表的配置，包括我们需要生成的数据库表，然后是对列的配置，包括主键配置，列表页配置，查询条件配置，编辑页面字段配置等

3）生成方案管理 主要负责代码生成管理，比如生成代码的包路径、访问路径、代码作者、代码注释信息等

