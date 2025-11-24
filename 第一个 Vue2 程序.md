
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

![img](https://tuchuangh-1386261756.cos.ap-guangzhou.myqcloud.com/ScreenShot_2025-11-23_201346_150.png?q-sign-algorithm=sha1&q-ak=AKIDynrLnf8NxuYpC8m7ojjaWeKL_3sEbD_oodycsNrwKLaGbfOGLWdX1ts83JnjEFpT&q-sign-time=1763903503;1763907103&q-key-time=1763903503;1763907103&q-header-list=host&q-url-param-list=ci-process&q-signature=8b3ec1799dc6b008eb7553cebd33f66f62983954&x-cos-security-token=nvo5fpBm5DGgZYScg1dBPj1nQvDFJ0faaaf4b943a3971e7083994487ed8e2779lpr7cqW__ZCYJHXbuiQr4HOYrbz2hVpZFhjrIDAnsY7eCh0WFDgrVpZY4KdBfqiH4PdvQM6hdEm4lXBUAN4fSAqaabPjGAYGVnPqZE-ounSrMF5JAIcduPW4e2JTuXujOHQ4nFc4KuYAdw2P6XcZvBeR-Wj3kxQX_kwNtrdxdNlUHfXtRMXksYR0RIQ6fNiwUxGnzkeVKvjBVN-14opG0qKJB6W4nC8Ds-zwr_apYxhyy5h5xKmVCUHLpyUsXNk5rdMzrvadjoJT7zzacQyrnw&ci-process=originImage)