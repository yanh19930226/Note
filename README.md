工具软件：墨刀原型，Processon在线画图软件，石墨文旦

158源码网:https://www.158code.com/welcome/search?keyword=VR 使用qq登入
Php：XMPP环境搭建：https://blog.csdn.net/web_xyk/article/details/80414662


CSS-NOTE:

1.去除移动端点击a链接的时候的背景颜色
    -webkit-tap-highlight-color: rgba(255, 255, 255, 0);
    -webkit-user-select: none;
    -moz-user-focus: none;
    -moz-user-select: none;
2.制作顶部导航时固定在顶部的样式
    position: sticky;
    position: -webkit-sticky;// 兼容 -webkit 内核的浏览器
    top: 10px;// 必须设一个值，否则不生效
3.CSS边框长度控制(elementui标签页修改默认的底部的标签选中状态)
    https://blog.csdn.net/Colossalis_c/article/details/71216339
4.移动端?使用css实现横向滚动(容器样式)
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    -webkit-box-align: middle;
    -ms-flex-align: middle;
    align-items: middle;
    overflow: auto;
5.CSS3实现左右布局
    display: flex;
    justify-content: space-between;//左右平均布局
6.去除img标签下的底部的像素,使用vertical-align:middle
7.实现经典的移动端商品两列布局

8.关于flex布局的语法和案例：http://www.ruanyifeng.com/blog/2015/07/flex-grammar.html
  以及css除了flex布局的其他的方式：https://blog.csdn.net/zhang6223284/article/details/81909600#23-flexbox-%E5%B8%83%E5%B1%80
  https://www.cnblogs.com/zhuzhenwei918/p/7147303.html
  https://www.cnblogs.com/imwtr/p/9648233.html
9.关于nth-of-type(n)和nth-child(n)的区别和解释：https://blog.csdn.net/weixin_41957484/article/details/80411082
10.关于清除浮动的介绍：https://www.jianshu.com/p/72846dc3cf00
11.移动开发一些特殊问题的解决：https://www.cnblogs.com/PeunZhang/p/3407453.html#meta
12.然绝对定位(absolute)的元素水平居中的方法：
方法一：（不能微调）
position:absolute;
left:0; right:0; top:0; bottom:0;
margin:auto;
方法二：（可微调）
position:absolute;
top:50%; left:50%;
margin-top:-100px;(元素高度的一半)
margin-left:-100px;(元素宽度的一半)
13.去除掉chrome的表单自动填充：
 在input type="password" 加上autocomplete="new-password"
  

Vue-NOTE(vue后台模板框架：https://gitee.com/smallweigit/avue)
1.关于vue-cli的创建
 npm install -g vue-cli
 vue init webpack name
 npm install 
 npm run dev
2.关于移动端点击事件的延迟处理办法
 方法一：静止缩放
 <meta name="viewport" content="width=device-width user-scalable= 'no'">
 方法二：fastclick.js
  FastClick 是 FT Labs 专门为解决移动端浏览器 300 毫秒点击延迟问题所开发的一个轻量级的库。简而言之，FastClick 在检测到touchend事件的时候，会通过 DOM 自定义事件立即触发一个模拟click事件，并把浏览器在 300 毫秒之后真正触发的click事件阻止掉。使用方法如下
  第一步：在页面中引入fastclick.js文件。
  第二步：在js文件中添加以下代码
  在 window load 事件之后，在body上调用FastClick.attach()即可
  
  window.addEventListener(function(){ 
    FastClick.attach( document.body );
  },false );
  滑动报Unable to preventDefault inside passive event listener的解决办法
  html{
   touch-action:none;
  }
  ABP相关知识
  
  学习Asp.netCore:http://www.manongjc.com/article/93003.html
      https://www.cnblogs.com/edisonchou/p/9124985.html
  1:abp中文社区：https://cn.abp.io/Templates
    52abp:https://www.52abp.com/wiki
    https://www.jianshu.com/u/cd2c97892d36
    关于如何在abp框架中添加新的业务的方法的文章：https://www.cnblogs.com/chillsrc/p/11024357.html
    abp-
    https://www.cnblogs.com/anyushengcms/p/8309115.html
    
    
    ABP配置权限简单：
    https://blog.csdn.net/wangwengrui40/article/details/86677672
    ABP设置默认的语言为中文
    http://www.bubuko.com/infodetail-2932180.html
    代码生成器：https://www.cnblogs.com/wer-ltm/p/5777978.html
    
    文章资料等:https://www.cnblogs.com/laozhang-is-phi/p/9541414.html
    
    
    
    LUNZ# 开发手册:http://ls-doc.lunztech.cn/
    麦扣官方文档：https://docs.xin-lai.com/#indexCard
    Asp.net Core:https://www.w3cschool.cn/netcore/netcore-hr9o31l0.html
    学习资料:http://www.csharpkit.com/2018-06-12_83909.html
    
    git配置sshkey:https://www.cnblogs.com/xiaohaojs/p/11160199.html
    
    Asp.NetCore基础：
    1.Individual authentication 模板:
      dotnet new mvc --help
      其中：
      -au|--auth                      The type of authentication to use
                  Individual       - Individual authentication
      
      -uld|--use-local-db        Whether to use LocalDB instead of SQLite. 
                                            This option only applies if --auth Individual or --auth IndividualB2C is specified.
                                            bool - Optional
      
                                            默认值: false/(*) true
      
      2、创建一个MVC项目
      ①dotnet new mvc -au Individual -uld --name IdentitySample
      ②用VS Code打开创建的MVC项目文件夹
      
      3、修改代码，并创建数据库
      ①修改appsettings.json的"DefaultConnection"连接字符串："Server=."
      然后初始化数据库：dotnet ef database update
      
     2.关于项目数据Identity MVC：DbContextSeed初始化:https://www.cnblogs.com/chongyao/p/9068007.html
    
    Identityserver：
    1.IdentityServer4默认暴露的一些endpoint等信息：http://localhost:5000/.well-known/openid-configuration
    2.IdentityServer客户端数据库的初始化命令：
      Add-Migration InitConfiguration -Context ConfigurationDbContext -OutputDir Data/Migrations/IdentityServer/ConfigurationDb
      Add-Migration InitPersisted -Context PersistedGrantDbContext -OutputDir Data/Migrations/IdentityServer/PersistedGrantDb
      Update-Database -Context ConfigurationDbContext
      Update-Database -Context PersistedGrantDbContext
    
    Docker(石墨文档):https://shimo.im/docs/anrlYMFEYloN52c8
    Docker参考文档：https://yeasy.gitbooks.io/docker_practice/content/
    
    windows安装mysql步骤：1.docker pull mysql 2.安装mysql配置用户名密码修改root密码和修改字符集命令：
    docker run -d -p 3306:3306 -e MYSQL_USER="yanh" -e MYSQL_PASSWORD="123" -e MYSQL_ROOT_PASSWORD="123" --name mysql mysql --character-     set-server=utf8 --collation-server=utf8_general_ci
    
    安装成功运行成功后，可以进入docker容器进行相应的操作
    1.进入容器：
    docker exec -it [ContainerName] bash
    //示例
    docker exec -it mysql bash
    2.进入mysql的命令行
      命令行进入mysql的root账户：
      mysql -uroot -p
      输入密码登入mysql
      use mysql 
      查看mysql的一些信息select user, host, plugin from user
      关于Mysql8.0以上用户登入名和密码加密错误还需要在多做一步操作;如果加密模式是sha2_cac,则需要修改加密的方式
      ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
      修改root的加密方式，对应的需要修改远程登入用户的加密方式
      
      修改用户的权限:
      GRANT ALL PRIVILEGES ON *.* TO 'test'@'localhost' WITH GRANT OPTION;
      
      
      
      windows:mysql挂载资料卷：
      
      1.提前在指定的目录下创建一个my.cnf文件,目录名最好为英文且不带特殊符号和空格,文件内容如下，注意：粘贴时要把每一行末尾的空格去除，否则运行时会报         错说utf8编码错误
        [mysqld]
        user=mysql
        character-set-server=utf8
        [client]
        default-character-set=utf8
        [mysql]
        default-character-set=utf8
  
        将文件所在的磁盘设为共享磁盘,这样docker才有权限对文件进行读写,方法:启动docker后,点
        击桌面右下角docker图标,右键选择settings,在SharedDrives 中勾选文件所在的磁盘,完成后docker需要重启
        图片: https://images-cdn.shimo.im/t4SsLcr5uqgbKLdh/image.png
        执行以下命令,磁盘路径(d:/mysql/config/my.cnf)需要根据自己配置文件所在的位置修改
        docker run -d -p 3306:3306 -e MYSQL_ROOT_PASSWORD =password123 -e   MYSQL_ROOT_HOST=% -v e:/mysql/config/my.cnf:/etc/my.cnf --           name mysql01 mysql/mysql-server

       4.使用 docker ps 查看是否启动,状态为 healthy 时 才算成功,然后通过以下命令进入容器
         docker exec -it mysql01 bash
         # 确认配置文件是否正确挂载

         # 确认root登录密码
         password123
         select user,host from user;

          5,最后可以用navicat 等外部工具测试是否能在外部正常连接docker图片: https://images-cdn.shimo.im/PxzNhEgXlhEipHAT/image.png
          图片: https://images-cdn.shimo.im/9FRX20jYPP4VsLjX/image.png
          图片: https://images-cdn.shimo.im/CLnM7HV5jtYTrqHF/image.png
          
          
          (亲测有效)
          所先创建相关文件夹与路径 
          c:/docker/mysql/config/my.cnf
          c:/docker/mysql/data
          需要使用官方mysql直接而不是使用mysql/mysql-server版本
          docker run -d -p 3306:3306 -e MYSQL_USER=sqltest -e MYSQL_PASSWORD=pwd123 -e MYSQL[mysqld]
          user=mysql
          character-set-server=utf8
          [client]
          default-character-set=utf8
          [mysql]
          default-character-set=utf8
          
          docker run -d -p 3306:3306 -e MYSQL_USER="yanh" -e MYSQL_PASSWORD="123" -e MYSQL_ROOT_PASSWORD="123" -e mysql_root_host=% -v c:develop/docker/mysql/config/my.cnf:/etc/my.cnf  -v c:develop/docker/mysql/data:/var/lib/mysql --name yanhsql mysql
      
      
      windows:mongo的创建和资料卷的挂载：
      --创建数据卷
      docker volume create --name mongodata
      --挂载数据卷运行mongo数据库
      docker run --name mongodb -v mongodata:/data/db -p 27017:27017 -d mongo:latest [--auth]

      注：测试使用，不需要账号权限不要加 --auth

      参数：
      docker run 运行容器
      --name mongodb 运行容器的名称为mongodb
      -v mongodata:/data/db 挂接保存数据的位置，冒号前面是本机（mongodata），后面是虚拟机中的映射目录（/data/db）
      -p 27017:27017 映射端口，前面是本机端口，后面是docker内的端口
      --auth 授权访问
      --登录镜像
      docker exec -it mongodb mongo admin
      --创建账号
      db.createUser({ 
        user: 'root', 
        pwd: 'admin', 
        roles: [ { role: "userAdminAnyDatabase", db: "admin" } ] 
      });
      --账号授权
      db.auth("root","admin");
    
    
    
    
    Linux上安装docker和Mysql的步骤思路：
    1.Linux上安装docker;2.linux上修改docker镜像源;3.linux安装mysql创建挂载资料卷目录配置;4.安装命令;
    5.修改root的密码和新建远程登入用户，可能需要修改加密方式;6.修改字符集后重启容器,查看字符集是否成功更改;7.删除容器测试是否挂载成功
    
    成功完成linux上安装docker mysql的安装和资料卷的挂载;关于linux 上安装docker的文章：https://www.cnblogs.com/myzony/p/9071210.html（保存到石     墨文档）
    成功在linux上安装mongo
    挂载都需要先在宿主上创建对应的文件和文件夹
    
    
    
    docker Console-->Dockerfile镜像制作：
    FROM microsoft/dotnet:sdk AS build-env
    WORKDIR /code

    COPY *.csproj /code
    RUN dotnet restore 

    COPY . /code
    RUN dotnet publish -c Release -o out

    FROM microsoft/dotnet:2.2-aspnetcore-runtime 
    WORKDIR /app

    COPY --from=build-env /code/out ./
    ENTRYPOINT [ "dotnet","console.dll"]
    制作命令：docker build -t yanh/consle:prod
    
    docker aspnetcore--->Dockerfile镜像制作：
    FROM microsoft/dotnet:2.2-sdk as build-env
    WORKDIR /code
    
    COPY *.csproj ./
    RUN dotnet restore
    
    COPY . ./
    RUN dotnet publish -c Releash -o out
    
    FROM microsoft/dotnet:2.2-aspnetcore-runtime 
    WORKDIR /app
    
    COPY --from=build-env /code/out ./
    
    EXPOSE 80
    ENTRYPOINT ["dotnet","User.API.dll"]
    制作命令并且使用DockerLink的方式实现aspnetcore程序镜像和Mysql镜像互联：
    1.制作：docker build -t yanh/aspnetcore:prod .
    2.互联：docker run -d -p 8002:80 --name aspnetcore --link mysql01:db yanh/aspnetcore:prod
    
    使用network实现数据库和程序互联：
    1.创建新的网络：docker network create -d bridge mybridge  docker network ls
    2.新建程序指定网络：docker run -d -p 8005:80 --net mybridge --name aspnetcore yanh/aspnetcore:prod
    (由于没有为数据库的连接配置文件添加资料卷,aspcore的镜像是基于link的,所以此时程序是退出状态)
    3.将mysql也添加到指定的网络中：docker network connect mybridge mysql01
    4.将mysql容器重新命名：docker rename mysql01 db
    5.重新启动程序容器，实现网络互联
    
    
    DockerCompose.yml文件实现asp.netcore和mysql:
    version: '3'
    services:
      db:（连接字符串也是叫db）
        image: mysql
        container_name: 'db'
        restart: always
        ports:
          - 3306:3306
        environment:
          MYSQL_ROOT_PASSWORD: 123
          MYSQL_USER: yanh
          MYSQL_PASSWORD: 123
        command:
          --default-authentication-plugin=mysql_native_password
          --character-set-server=utf8mb4
          --collation-server=utf8mb4_general_ci
          --explicit_defaults_for_timestamp=true
          --lower_case_table_names=1
        volumes:#资料卷的挂载（这时外部的文件一定要有数据）
          - /e/docker/mysqlcompose/mysql-init:/docker-entrypoint-initdb.d
          - /e/docker/mysqlcompose/data:/var/lib/mysql
        networks:
           - my-bridge
      web:
        build: 
          context: .
          dockerfile: Dockerfile  #指定使用的Dockerfile
        container_name: 'myaspnetcore'
        ports:
           - '8000:80'
        depends_on:
           - db
        volumes:#资料卷的挂载（这时外部的文件一定要有数据）
           - /e/docker/mysqlcompose/appsettings.json:/app/appsettings.json
        networks:
           - my-bridge
    networks:
      my-bridge: #创建名为mybridge的network
        driver: bridge
        
     RabbitMQ安装：docker run -d --hostname my-rabbit --name rabbit -p 5672:5672 -p 15672:15672 rabbitmq:3-management   
        
    GitLab的安装：
    1.linux:https://docs.gitlab.com/omnibus/docker/#run-the-image
    2.gitlab502的解决访问：内存不足，添加虚拟内存
    测试访问的时候老是提示502，原因在于我的服务器只有1G的内容，不满足gitlab运行的最低配置,gitlab最低的运行内存要求是2GB,配置的虚拟内存来解决问题
    
    sudo dd if=/dev/zero of=/swapfile bs=1024 count=2048k
    sudo mkswap /swapfile
    sudo swapon /swapfile
    sudo vim /etc/fstab
    添加内容
    
    /swapfile none swap defaults 0 0
    这就解决问题了
    
    Windows下安装gitlab,没有配置资料卷
    docker run -d --hostname localhost --publish 8443:443 --publish 8118:80 --publish 8022:22 --name gitlab --privileged=true --restart     always  gitlab/gitlab-ce:latest
    
    
    
    Asp.Net Core 3.0 集成SwaggerUI:https://www.cnblogs.com/taotaozhuanyong/p/11602820.html
    
    User.Api
    1.关于解决efcore操作mysql,出现System.InvalidOperationException:“No coercion operator is defined between types 'System.Int16' and          'System.Boolean'.”的问题:使用Pomelo.EntityFrameworkCore.MySql 
    2.efcore自动生成自增长主键：fluentapi ValuesGenerateAddOn
    3.在dotnet 2.1 新建的webapi项目创建的ValuesController默认是 集成BaseController，没有Json方法，修改集成Controller即可
    



.NetCore测试XUnit测试：https://www.cnblogs.com/tylerzhou/p/11403854.html


Linux服务器操作命令：uname -r 查看centos系统内核版本
    关于centos8系统上面安装docker:https://blog.csdn.net/TianXieZuoMaiKong/article/details/104521439
    
           
    
    
  
 
    

    
