# RESUME
> 参考了 http://strml.net/ 的样式效果

> 预览地址: https://huangshouqi.github.io/resume

> 另外还发现一个[vue版本](https://github.com/jirengu-inc/animating-resume)的也很不错

## 思路
采用setInterval改变body和style的innnerHTML实现动态加载的打字机效果

## 示例
```javascript
html
<pre><div id="content"></div></pre>
<style id="style"></style>
script
var content = document.getElementById('content')
var style = document.getElementById('style')
var code = `
Hello World!
My name is Archie!
`
var n = 0;
setInterval(()=>{
	content.innerHTML = code.substring(0,n) 
	style.innerHTML = code.substring(0,n)
	n = n + 1
},30)
```
