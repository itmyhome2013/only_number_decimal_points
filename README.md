JSʵ��ֻ���������ֺ�С����
============

```html
<input type="text" value=""  onkeyup="onlyNumber(this)" onblur="onlyNumber(this)"/> 	
```

```js
<script type="text/javascript">

function onlyNumber(obj) {
	//�õ���һ���ַ��Ƿ�Ϊ����
	var t = obj.value.charAt(0);
	//�Ȱѷ����ֵĶ��滻�����������ֺ�. 
	obj.value = obj.value.replace(/[^\d\.]/g, '');
	//���뱣֤��һ��Ϊ���ֶ�����. 
	obj.value = obj.value.replace(/^\./g, '');
	//��ֻ֤�г���һ��.��û�ж��. 
	obj.value = obj.value.replace(/\.{2,}/g, '.');
	//��֤.ֻ����һ�Σ������ܳ����������� 
	obj.value = obj.value.replace('.', '$#$').replace(/\./g, '').replace(
			'$#$', '.');
	//�����һλ�Ǹ��ţ����������
	if (t == '-') {
		obj.value = '-' + obj.value;
	}
}
	
</script>
```

��ʾ��ַ: <a href="http://blog.itmyhome.com/only_number_decimal_points/" target="_blank">���</a>