xScroll - touch版向下拉动刷新、向上拉动加载更多

## css

body{padding:0;margin:0;background:#999;}
.main{position:relative;height:auto;background: #999;}
.main-body{position: absolute;top:0;left:0;background: #fff;width:100%;z-index: 2;height:1000px;}
.toptip{position: absolute;top:30px;left:25%;z-index: 1;right: 25%;text-align: center;}
.downtip{position: absolute;bottom:30px;left:25%;z-index: 1;right: 25%;text-align: center;}
.hide{display:none;}

## html

div class="main"
  div class="toptip hide" toptip /div
  div class="main-body"&gl;&tl;/div
  div class="downtip hide" downtip /div
/div

## jQuery

jquery.2.1.3.js

## 使用

jQuery("body").xScroll({

  向下拉动动作 - 刷新

  tophandle: function(end) {

    动作结束方法

    end();
  },

  向上拉动动作 - 加载更多

  downhandle: function(end) {

    动作结束方法

    end();
  }
});

或者

只是一个带弹性的页面

jQuery("body").xScroll();

也可以这样使用

window.xScroll();

以及

var xScroll = require("xscroll");

xScroll();

## 提供方法

refresh 刷新初始化

hasTouch 是否支持touch

orientation 判断是否横、竖屏

showtoptip 显示上面的提示

showdowntip 显示下面的提示

