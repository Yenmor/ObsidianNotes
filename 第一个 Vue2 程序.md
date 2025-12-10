
- # 在文件开头引入 Vue

```js
<script src = "../js/vue.js"></script>
``` 

- # 创建 Vue 托管的容器

```html
<div id="app"> </div>
```

- # 创建 Vue 并挂载到 id 为 app 的 html 元素上

```js
	new Vue({
		template : '<h1>{{msg}}</h1>',
		data : {
			msg : 'Hello World'
		}
	}).$mount('#app')
```

- # 完整代码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <div id="app"> </div>
    <script src = "../js/vue.js"></script>
    <script>
	        new Vue({
	            template : '<h1>{{msg}}</h1>',
	            data : {
	                msg : 'Hello World'
	            }
	        }).$mount('#app')
    </script>
</body>
</html>
```

- # 运行结果
***

<img src="https://tuchuangh-1386261756.cos.ap-guangzhou.myqcloud.com/blog/20251124221551657.png" width = 40%>