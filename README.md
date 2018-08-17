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
绘制文本：

```JavaScript
//绘制数字12
 ctx.font = "bold 14px Arial";
            ctx.textAlign = "center";
            ctx.textBaseline = "middle";
            ctx.fillText ("12",100,20);
```

变换：

```JavaScript
            ctx.fillStyle = "#ff0000";
            ctx.save();//第一次调用save()，设置一个栈

            ctx.fillStyle = "#00ff00";
            ctx.translate(100,100);//移动原点
            ctx.save();//第二次调用save()，设置第二一个栈

            ctx.fillStyle = "#0000ff";
            ctx.fillRect(0,0,100,100);//原点在（100，100）绘制蓝色矩形

            ctx.restore();//调用restore()方法，栈结构向前返回一级
            ctx.fillRect(10,10,100,100);//原点在（100，100）绘制绿色矩形

            ctx.restore();//调用restore()方法，栈结构向前返回一级
            ctx.fillRect(0,0,100,100);//原点在（0，0）绘制红色矩形
```
      


绘制图像
```JavaScript
//事先在html中用<img>元素插入图片
var drawing = document.getElementById("drawing");
        var ctx = drawing.getContext("2d");
        var img = document.getElementById("myImg");
        ctx.drawImage(img,10,10,500,500);
```
