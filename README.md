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
    
    
    Asp.net Core:https://www.w3cschool.cn/netcore/netcore-hr9o31l0.html
    
    
    
    
    Docer:
    windows 家庭版安装https://www.jianshu.com/p/2aa5b05717c6
    
    
    windows安装mysql步骤：1.docker pull mysql 2.安装mysql配置用户名密码修改root密码和修改字符集命令：
    docker run -d -p 3306:3306 -e MYSQL_USER="yanh" -e MYSQL_PASSWORD="123" -e MYSQL_ROOT_PASSWORD="123" --name mysql mysql --character-set-server=utf8 --collation-server=utf8_general_ci
    
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
    
     
     
     
     
      windows:mysql挂载资料卷：
    
    
    
    
    Linux上安装docker;linux上修改docker镜像源;linux安装mysql创建挂载资料卷目录配置;安装命令;
    修改root的密码;新建远程登入用户;可能需要修改加密方式;修改字符集；删除容器测试是否挂载成功
    
    
   成功完成linux上安装docker mysql的安装和资料卷的挂载；
   关于linux 上安装docker的文章：https://www.cnblogs.com/myzony/p/9071210.html
    
    
           
    
    
  
 
    

    
