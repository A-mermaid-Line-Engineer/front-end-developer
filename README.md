# front-end-developer
#html
#使用 jquery-3.2.1.min.js
<!doctype html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<link rel="stylesheet" type="text/css" href="css.css">
	<script type="text/javascript" src="jquery-3.2.1.min.js"></script>

	<script type="text/javascript">
$(document).ready(function(){

	 	$(window).scroll(function(){
	 		var window_height = $(window).scrollTop();

	 		if (window_height >= 440) {
	 			$(".main .nav").addClass("navone");
	 			$(".main .xiamiande").css("display","block");
	 		}     //这里不能加冒号！！
	 		else{
	 			$(".main .nav").removeClass("navone");
	 			$(".main .xiamiande").css("display","none");
	 		}
	 	});

	 	//点击添加红色背景
	 	$(".part_1").click(function(){
	 		$(this).addClass("current").siblings().removeClass("current")
	 	})
	 	$(".part_2").click(function(){
	 		$(this).addClass("current").siblings().removeClass("current")
	 	})
	 	$(".part_3").click(function(){
	 		$(this).addClass("current").siblings().removeClass("current")
	 	})
	 	$(".part_4").click(function(){
	 		$(this).addClass("current").siblings().removeClass("current")
	 	})
	 	$(".part_5").click(function(){
	 		$(this).addClass("current").siblings().removeClass("current")
	 	})
	 	$(".part_6").click(function(){
	 		$(this).addClass("current").siblings().removeClass("current")
	 	})

	 	//点击windows滑动动画
		$(".part_2").on("click",function(){
            var H=$("#part_2").offset().top;
			$("body").animate({"scrollTop":H},800);
		})
		$(".part_3").on("click",function(){
            var H=$("#part_3").offset().top;
			$("body").animate({"scrollTop":H},800);
		})
		$(".part_4").on("click",function(){
            var H=$("#part_4").offset().top;
			$("body").animate({"scrollTop":H},800);
		})
		$(".part_5").on("click",function(){
            var H=$("#part_5").offset().top;
			$("body").animate({"scrollTop":H},800);
		})
		$(".part_6").on("click",function(){
            var H=$("#part_6").offset().top;
			$("body").animate({"scrollTop":H},800);
		})
		$(".part_1").on("click",function(){
            var H=$("#part_1").offset().top;
			$("body").animate({"scrollTop":H},800);
		})


//随滚动条滑动nav的current背景色移动
		$(window).scroll(function(){
	 		var part_2 = $("#part_2").offset().top,
	 			part_3 = $("#part_3").offset().top,
	 			window_height = $(window).scrollTop();

	 		if (part_3 >= window_height >= part_2) {
	 			$(".mian ul .part_2").addClass("current").siblings().removeClass("current");
	 		}
	 	});
console.log($(window).scrollTop())
console.log($("#part_2").offset().top)
console.log($("#part_3").offset().top)
})


	</script>
</head>
<body>
<div class="main">
    <div class="zhanweizhi">我来占位置</div>
    <div class="h40"></div>
	<div class="nav">
		<ul class="navbox">
			<li class="part_1 current"><a href="#part_1">产品介绍</a></li>
			<li class="part_2"><a href="#part_2">性能优势</a></li>
			<li class="part_3"><a href="#part_3">技术参数</a></li>
			<li class="part_4"><a href="#part_4">相关案例</a></li>
			<li class="part_5"><a href="#part_5">其他型号</a></li>
			<li class="part_6"><a href="#part_6">在线订购</a></li>
		</ul>
	</div>
	<div class="clear"></div>
	<!-- 添加空白div -->
	<div class="xiamiande"></div>
	<div class="h40 part" id="part_1"></div>
	<div class="cpjs">
		<p>我是一段话</p>
		<p>我是另一段话</p>
		<p>我是第三段话</p>
		<p>我们全都是话</p>
		<div class="zhanweizhi">我来占位置</div>
	</div>
	<div class="h40 part" id="part_2"></div>
	<div class="xnys">
		<p>我是一段话</p>
		<p>我是另一段话</p>
		<p>我是第三段话</p>
		<p>我们全都是话</p>
		<div class="zhanweizhi">我来占位置</div>
	</div>
	<div class="h40 part" id="part_3"></div>
	<div class="jscs">
		<p>我是一段话</p>
		<p>我是另一段话</p>
		<p>我是第三段话</p>
		<p>我们全都是话</p>
		<div class="zhanweizhi">我来占位置</div>
	</div>
	<div class="h40 part" id="part_4"></div>
	<div class="xgal">
		<p>我是一段话</p>
		<p>我是另一段话</p>
		<p>我是第三段话</p>
		<p>我们全都是话</p>
	</div>
	<div class="h40 part" id="part_5"></div>
	<div class="qtxh">
		<p>我是一段话</p>
		<p>我是另一段话</p>
		<p>我是第三段话</p>
		<p>我们全都是话</p>
		<div class="zhanweizhi">我来占位置</div>
	</div>
	<div class="h40 part" id="part_6"></div>
	<div class="zxdg">
		<p>我是一段话</p>
		<p>我是另一段话</p>
		<p>我是第三段话</p>
		<p>我们全都是话</p>
		<div class="zhanweizhi">我来占位置</div>
	</div>
</div>	
</body>
</html>

#css
a,li{text-decoration: none;list-style: none;color: #333}
*{padding:0;margin: 0}
.clear{clear: both;}
.main{
	width: 1000px;
	margin: 0 auto;
	position: relative;
}
.zhanweizhi{
	width: 100%;
	height: 400px;
	background: #333;
}
.h40{
	height: 45px;
}

.navbox li{
	float: left;
	width: 16.667%;
	height: 45px;
	text-align: center;
	cursor: pointer;
	line-height: 45px;
	background: #ccc
}
.navbox .part a{
	display: block;
}
.navbox .current{
	background: #ff3f3c;
	color: #fff;
}
.nav{
	position: relative;
	height: 45px;
	width: 1000px;
}
.navone{
	position: fixed;
	top: 0;
}

.xiamiande{
	height: 45px;
	width: 100%;
	display: none;
}
