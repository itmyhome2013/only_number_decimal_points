JS实现倒计时
============

```html
<input type="text" class="form-control" style="width: 200px;" 
	   id="idCard" placeholder="输入校验码">
<button id="code" class="btn btn-default" onclick="getCode();">获取校验码</button>
```

```js
var i;
function getCode(){
	$("#code").attr({"disabled":"disabled"});
	i = self.setInterval("countdown()", 1000);
}

var int = 10
function countdown() {
	document.getElementById("code").innerHTML = int + "秒后重新发送";
	int--;
	if(int<0){
		i=window.clearInterval(i)//结束
		int = 10; //重新赋值
		$("#code").removeAttr("disabled").html("重新获取校验码");//将按钮可用
	}
}
```

演示地址: <a href="http://itmyhome.com/countdown/" target="_blank">点击</a>