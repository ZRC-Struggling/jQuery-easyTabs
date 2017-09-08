# jQuery-easyTabs

### 简介
　　这是一个简易的选项卡插件，代码量仅3KB，灵活易用，支持动画，可配置触发切换的事件类型

### 效果截图
![demo1](https://raw.githubusercontent.com/ZRC-Struggling/jQuery-easyTabs/master/demos/imgs/demo1.jpg)

### 用法示例
- 引入样式表
```
<link rel="stylesheet" type="text/css" href="../src/jQuery.easyTabs.css">
```
- 构建HTML结构
```
<div class="simple-tab">
    <ul>
    	<li class="active">tabTitle1</li>
        <li>tabTitle2</li>
        <li>tabTitle3</li>
        ...
    </ul>
    <div>
    	<div class="active">tabContent1</div>
   		<div>tabContent2</div>
   		<div>tabContent3</div>
		...
    </div>
</div>
```

- 引入jQuery库
```
<script type="text/javascript" src="../jquery/jquery-2.2.3.js"></script>
```
- 引入插件
```
<script type="text/javascript" src="../src/jQuery.easyTabs.js"></script>
```

- 调用插件
```
<script>
$(function () {
    $(".simple-tab").tabs(options);
})
</script>
```
### 说明
1. HTML结构：
    1) 外层必须是class为"simple-tab"的div，该div内有"ul>li"和"div>div"结构
    2) ul里面的li作为选项卡标题,并且第一个li要加上"active"类名
    3) div里面的div作为选项卡内容，并且第一个div要加上"active"类名

2. options对象可接收的参数：
    1) type: 用于设置触发选项卡切换的事件类型，默认为"mouseover"
    2) speed: 用于设置切换的时间，默认为0，单位为毫秒
    3) animation: 用于设置动画的类型，只接收三个值("toogle", "slide", "fade")，默认为"toogle"
         toogle: 等同于调用jQuery的show()
	 slide: 等同于调用jQuery的slideDown()
	 fade: 等同于调用jQuery的fadeIn()
	
3. animation只针对切换之后出现的tab，不管怎么样，切换之前的tab都会立即消失。
