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
    

    