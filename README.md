JSʵ�ֵ���ʱ
============

```html
<input type="text" class="form-control" style="width: 200px;" 
	   id="idCard" placeholder="����У����">
<button id="code" class="btn btn-default" onclick="getCode();">��ȡУ����</button>
```

```js
var i;
function getCode(){
	$("#code").attr({"disabled":"disabled"});
	i = self.setInterval("countdown()", 1000);
}

var int = 10
function countdown() {
	document.getElementById("code").innerHTML = int + "������·���";
	int--;
	if(int<0){
		i=window.clearInterval(i)//����
		int = 10; //���¸�ֵ
		$("#code").removeAttr("disabled").html("���»�ȡУ����");//����ť����
	}
}
```

��ʾ��ַ: <a href="http://itmyhome.com/countdown/" target="_blank">���</a>