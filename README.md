

# 网站开发报告
## 关于此网站
### 本网站是一个对NBA进行介绍的网站，由于本人喜欢篮球，其中大部分内容包括文字图片都是来源于网络，只是为了拿来当作业素材，本人承诺不会将此网站用于商业，若有侵权，不慎抱歉！！！

---
## 为什么要做本网站
### 1、为了检验web前端开发课程一学期的学习成果。
### 2、为了向大家展示我的个人兴趣爱好。
### 3、同时向更多的人展示NBA，了解NBA。
---

## 资料来源
### 大部分资源来自NBA中文网站，文字内容来自百度文库。![image](https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1496458765599&di=784d1166168eda4ca23852b3f16f23b2&imgtype=0&src=http%3A%2F%2Fs7.cdn.deahu.com%2Fjingyan%2Fimage_cluster%2F2015-01-28%2F1%2F3757476_F7E52EC65718E03F0469710228E59215.jpg)![image](https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1496458811881&di=0dc7f3d1d3485d949f93f3b30fcd8975&imgtype=0&src=http%3A%2F%2Fimgs.technews.cn%2Fwp-content%2Fuploads%2F2014%2F10%2FBaidu.jpg)
---
## 兼容的浏览器
### 谷歌 火狐 IE9等
---
## 创作过程
### 本来刚开始对网页制作一窍不通，但后来也渐渐熟悉起来，有不懂的地方就问同学老师，或者自己摸索，虽然最后网页效果也不是很美观，但我也很满足，希望以后在WEB这一类的课上能越学越好，自己能做出更好的网页来。
---
## 用到的元素和功能及网页的构成
### 页面组成：首页（涵盖列表页)[点此](index.html/) 表单页 详细页 自我介绍页
---
### HTML标记
#### 元标记:title、meta
#### 语义类标记 h1-h2、p、em、pre、code、ul、table
#### 媒体类标记 a、img
#### 容器类标记 div、span、article、section、header、main、footer、section、aside、nav
#### 表单及其控件：form、input、textarea、select、submit
### CSS知识点
#### 基本排版：各html标记的基本样式设置
#### 图标字体icon font
#### 横向布局：使用浮动方式实现
#### 定位：绝对定位或固定定位背景与边框
#### css特效：2D转换或过渡
#### 杂项：text-aglin、display等属性的使用
### javascript
#### 使用jquery插件实现一个特效
#### 自行开发JS脚本实现一个特效
---
## 技术点说明
### 1、页面排版问题及解决代码
本次页面设计总共分为三部分
```
<nav style="width: 100%;height: 50px;display: block;">
</nav>
<div class="sidebar" style="width: 15%;height:1300px;background: #0080FF;float: left;">
</div>
<div class="container" style="width: 85%;height: 1300px;float:left;">
</div>
```
### 2、背景图片及其插入

```
background:url(./images/bg.jpg)
```
### 3、jquery特效的引用及js特效的开发

```
<script type="text/javascript">
window.onload = function(){
	var star = document.getElementsByTagName('a');
	var oDiv = document.getElementsByTagName('div')[0];
	var temp = 0;
	
	for(var i = 0, len = star.length; i < len; i++){
		star[i].index = i;
		
		star[i].onmouseover = function(){
			clear();
			for(var j = 0; j < this.index + 1; j++){
				star[j].style.backgroundPosition = '0 0';
			}
		}
		
		star[i].onmouseout = function(){
			for(var j = 0; j < this.index + 1; j++){
				star[j].style.backgroundPosition = '0 -20px';
			}
			current(temp);
		}
		
		star[i].onclick = function(){
			temp = this.index + 1;
			document.getElementsByTagName('p')[0].innerHTML = temp + ' 颗星';
			current(temp);
		}
	}
	//清除所有
	function clear(){
		for(var i = 0, len = star.length; i < len; i++){
			star[i].style.backgroundPosition = '0 -20px';
		}
	}
	//显示当前第几颗星
	function current(temp){
		for(var i = 0; i < temp; i++){
			star[i].style.backgroundPosition = '0 0';
		}
	}
};
</script>
```
## 开发心得体会
### 让我体会到了网站设计的无穷魅力，同时也让我体会了编程的幸苦和繁琐，但我一定会克服困难，努力将自己的兴趣爱好转向这一方面。

