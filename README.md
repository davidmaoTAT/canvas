# canvas
绘制图像

绘制矩形：
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
           
绘制路径：
```javascript
              // 开始路径
        var drawing = document.getElementById("drawing");
        if(drawing.getContext){
            ctx.beginPath();

            // 绘制外圆
            ctx.arc(100,100,99,0,2*Math.PI,false);

            // 绘制内圆
            ctx.moveTo(194,100);
            ctx.arc(100,100,94,0,2*Math.PI,false);

            // 绘制分钟
            ctx.moveTo(100,100);
            ctx.lineTo(100,15);

            // 绘制时钟
            ctx.moveTo(100,100);
            ctx.lineTo(35,100);

            // 描边路径
            ctx.stroke();
            
             // 判断一个点在不在路径上
            if(ctx.isPointInPath(100,99)){
                alert("yes");
            }
          ｝
 
```
           
      



