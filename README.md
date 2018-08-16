# canvas
绘制图像
```javascript
var drawing = document.getElementById("drawing");
        if(drawing.getContext){
            var ctx = drawing.getContext("2d");
            //绘制红色矩形
            ctx.fillStyle = "#FF0000";
            ctx.fillRect (10,10,50,50);
            //绘制半透明蓝色矩形
            ctx.fillStyle = "rgba(0,0,255,0.5)"
            ctx.fillRect(30,30,50,50);
            //绘制红色描边矩形，没有填充颜色
            ctx.strokeStyle = "#ff0000";
            ctx.strokeRect(80,80,50,50);
            //清除一个矩形
            ctx.clearRect(20,20,50,50);
        }
```
