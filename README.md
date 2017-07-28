## 图片轮播

1. Flexslider图片轮播、文字图片相结合滑动切换效果
2. Flexslider官网地址：[http://www.woothemes.com/flexslider/](http://www.woothemes.com/flexslider/)

> Flexslider是一款基于的jQuery内容滚动插件。它能让你轻松的创建内容滚动的效果，具有非常高的可定制性。开发者可以使用Flexslider轻松创建各种图片轮播效果、焦点图效果、图文混排滚动效果。

- #### Flexslider具有以下特性：

  - 支持滑动和淡入淡出效果。
  - 支持水平、垂直方向滑动。
  - 支持键盘方向键控制。
  - 支持触控滑动。
  - 支持图文混排，支持各种html元素。
  - 自适应屏幕尺寸。
  - 可控制滑动单元个数。
  - 更多选项设置和回调函数。

- #### HTML

```header
<link rel="stylesheet" type="text/css" href="flexslider.css" /> 
<script type="text/javascript" src="jquery-1.7.2.min.js"></script> 
<script type="text/javascript" src="jquery.flexslider-min.js"></script>
```

```body
<div class="flexslider"> 
      <ul class="slides"> 
        <li><img src="images/s1.jpg" /></li> 
        <li><img src="images/s2.jpg" /></li> 
        <li><img src="images/s3.jpg" /></li> 
        <li><img src="images/s4.jpg" /></li> 
      </ul> 
</div>
$(function() { 
    $(".flexslider").flexslider(); 
});     
```

- #### FlexSlider插件的详细设置参数####

```
$(window).load(function() {
 $('.flexslider').flexslider({
  animation: "fade",              //String: Select your animation type, "fade" or "slide"图片变换方式：淡入淡出或者滑动
  slideDirection: "horizontal",   //String: Select the sliding direction, "horizontal" or "vertical"图片设置为滑动式时的滑动方向：左右或者上下
  slideshow: true,                //Boolean: Animate slider automatically 载入页面时，是否自动播放
  slideshowSpeed: 7000,           //Integer: Set the speed of the slideshow cycling, in milliseconds 自动播放速度毫秒
  animationDuration: 600,         //Integer: Set the speed of animations, in milliseconds动画淡入淡出效果延时
  directionNav: true,             //Boolean: Create navigation for previous/next navigation? (true/false)是否显示左右控制按钮
  controlNav: true,               //Boolean: Create navigation for paging control of each clide? Note: Leave true for manualControls usage是否显示控制菜单
  keyboardNav: true,              //Boolean: Allow slider navigating via keyboard left/right keys键盘左右方向键控制图片滑动
  mousewheel: false,              //Boolean: Allow slider navigating via mousewheel鼠标滚轮控制制图片滑动
  prevText: "Previous",           //String: Set the text for the "previous" directionNav item
  nextText: "Next",               //String: Set the text for the "next" directionNav item
  pausePlay: false,               //Boolean: Create pause/play dynamic element
  pauseText: 'Pause',             //String: Set the text for the "pause" pausePlay item
  playText: 'Play',               //String: Set the text for the "play" pausePlay item
  randomize: false,               //Boolean: Randomize slide order 是否随即幻灯片
  slideToStart: 0,                //Integer: The slide that the slider should start on. Array notation (0 = first slide)初始化第一次显示图片位置
  animationLoop: true,            //Boolean: Should the animation loop? If false, directionNav will received "disable" classes at either end 是否循环滚动
  pauseOnAction: true,            //Boolean: Pause the slideshow when interacting with control elements, highly recommended.
  pauseOnHover: false,            //Boolean: Pause the slideshow when hovering over slider, then resume when no longer hovering
  controlsContainer: "",          //Selector: Declare which container the navigation elements should be appended too. Default container is the flexSlider element. Example use would be ".flexslider-container", "#container", etc. If the given element is not found, the default action will be taken.
  manualControls: "",             //Selector: Declare custom control navigation. Example would be ".flex-control-nav li" or "#tabs-nav li img", etc. The number of elements in your controlNav should match the number of slides/tabs.自定义控制导航
  manualControlEvent:"",          //String:自定义导航控制触发事件:默认是click,可以设定hover
  start: function(){},            //Callback: function(slider) - Fires when the slider loads the first slide
  before: function(){},           //Callback: function(slider) - Fires asynchronously with each slider animation
  after: function(){},            //Callback: function(slider) - Fires after each slider animation completes
  end: function(){}               //Callback: function(slider) - Fires when the slider reaches the last slide (asynchronous)
  
 });
});
```



- #### Flexslider选项设置

| 参数             | 描述                                       | 默认值          |
| -------------- | ---------------------------------------- | ------------ |
| animation      | 动画效果类型，有"fade"：淡入淡出，"slide"：滑动           | "fade"       |
| easing         | 内容切换时缓动效果，需要jquery easing插件支持            | "swing"      |
| direction      | 内容滚动方向，有"horizontal"：水平方向 和"vertical"：垂直方向 | "horizontal" |
| animationLoop  | 是否循环滚动                                   | true         |
| startAt        | 初始滑动时的起始位置，定位从第几个开始滑动                    | 0            |
| slideshow      | 是否自动滑动                                   | true         |
| slideshowSpeed | 滑动内容展示时间(ms)                             | 7000         |
| animationSpeed | 内容切换时间(ms)                               | 600          |
| initDelay      | 初始化时延时时间                                 | 0            |
| pauseOnHover   | 鼠标滑向滚动内容时，是否暂停滚动                         | false        |
| touch          | 是否支持触摸滑动                                 | true         |
| directionNav   | 是否显示左右方向箭头按钮                             | true         |
| keyboard       | 是否支持键盘方向键操作                              | true         |
| minItems       | 一次最少展示滑动内容的单元个数                          | 1            |
| maxItems       | 一次最多展示滑动内容的单元个数                          | 0            |
| move           | 一次滑动的单元个数                                | 0            |
| 回调函数           | start: function(){},            before: function(){},           after: function(){},            end: function(){},            added: function(){},            removed: function(){},            init: function(){}, | -            |

