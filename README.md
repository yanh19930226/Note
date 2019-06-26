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
  

Vue-NOTE
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
  
 
    

    
