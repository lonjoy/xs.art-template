# xs.art-template [![spm version](http://spmjs.io/badge/xs.art-template)](http://spmjs.io/package/xs.art-template)

---

An awesome spm package!

---

## Install

```
$ spm install xs.art-template --save
```

## Usage

```html
<!DOCTYPE html>
<html>
<head>
	<title></title>
</head>
<body>

<script id="test" type="text/html">
	<h1>{{title}}</h1>
	<ul>
		{{each list as value i}}
		<li>索引 {{i + 1}} ：{{value}}</li>
		{{/each}}
	</ul>
</script>

<div id="content"></div>

<script type="text/javascript" src="/sea-modules/seajs/2.3.0/dist/sea.js"></script>

<script type="text/javascript">
	seajs.config({
		base: '/dist/'
	});
</script>

<script type="text/javascript">
	seajs.use('app/1.0.0/index');
</script>

</body>
</html>
```

```js
var template = require('xs.art-template');

var data = {
	title: '标签',
	list: ['文艺', '博客', '摄影', '电影', '民谣', '旅行', '吉他']
};
var html = template('test', data);
document.getElementById('content').innerHTML = html;
```
