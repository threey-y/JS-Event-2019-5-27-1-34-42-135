## 要求 
    
- 实现一个基础的计时器应用，点击开始按钮开始计时，点击结束按钮结束计时，并把计时的结果显示在上面的输入框中。

```html
  <!DOCTYPE html>
  <html lang="en">
  <head>
      <meta charset="UTF-8">
      <title>定时器示例</title>
  </head>
  <body>
  
  <input type="text" id="result">
  
  <input type="button" value="开始" >
  <input type="button" value="结束" >
  
  <script>
function showTime(){
        var d = new Date();
        var year = d.getFullYear();
        var month = d.getMonth();
        var dat = d.getDate();
        var hour = d.getHours();
        var minutes = d.getMinutes();
        var seconds = d.getSeconds();
        document.getElementById("result").innerHTML =
         year +"年" +(month + 1) +"月"+
         dat+"日"+hour+"时"+minutes+"分"+seconds+"秒";
    }
    var a;
    function startTime(){
        a = setInterval("showTime()",1000);
    }

    function stopTime(){
        clearInterval(a);
    }
  </script>
  </body>
  </html>
```
