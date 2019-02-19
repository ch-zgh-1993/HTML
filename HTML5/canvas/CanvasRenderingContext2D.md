/*
* @Author: Zhang Guohua
* @Date:   2019-02-19 10:19:35
* @Last Modified by:   zgh
* @Last Modified time: 2019-02-19 11:03:51
* @Description: create by zgh
* @GitHub: Savour Humor
*/
# CanvasRenderingContext2D


## 属性，方法分类：

- 矩形： 
    + clearRect(): 清除指定区域内部所有像素信息，变为初始色，透明。
    + fillRect(): 填充矩形。颜色，渐变，图案。
    + strokeRect(): 矩形描边。
     
- 文本：
    + fillText(): 填充文本。
    + strokeText(): 文字描边。
    + measureText(): 文字测量。返回TextMetrics对象，该对象的width属性值就是字符占据的宽度。
     
         
- 线条样式：
    + lineCap: butt(无端帽), round(圆形端帽), square(方形端帽)。 线端点样式。
    + lineDashOffset: 虚线偏移距离
    + lineJoin: 线转角样式，miter(尖角), round(圆角), bevel(平角);
    + lineWidth: 线宽。主要用于描边。
    + miterLimit: 规定线转角为 miter 时，出现尖角的长度范围。尖角限制比率。线条的尖角如果没有限制，在线条粗角度小的情况下会很长很长，因此，需要一个限制比率。默认是10。
    + getLineDash(): 返回当前虚线数值。返回值是一个偶数个数的数组。
    + setLineDash(): 设置线条为虚线。

- 文本样式：
    + font: 字号， 字体。设置字体相关样式，包括字号，字体信息。默认值是10px sans-serif。
    + textAlign: 指定文本水平对齐方式。start（默认值），end，left，right以及center。
    + textBaseLine: 设置文本基线对齐方式。支持属性值有：top，hanging，middle，alphabetic（默认值），ideographic，bottom。
    + direction: 设置文本显示方向。支持属性值有：inherit（默认值），ltr和rtl。
     
- 填充和描边：
    + fillStyle: 填充样式。 颜色， 渐变， 图片/纹理。
    + fill(): 填充。
    + strokeStyle: 描边样式。 可以是路径， 形状，文字的描边。可以是颜色， 渐变，图案。
    + stroke(): 描边。
     
- 渐变相关：
    + createLinearGradient(): 创建线性渐变。  渐变色等。
    + createRadialGradient(): 创建径向渐变。 
     
- 图案相关：
    + createPattern(): 创建图案。图案内容可以是图片，可以是<canvas>元素，也可以是渐变。此方法返回CanvasPattern对象。
     
- 阴影相关：
    + shadowBlur: 阴影模糊程度。 默认0；
    + shadowColor: 阴影颜色。默认全透明黑色。
    + shadowOffsetX: 阴影水平偏移，默认0；
    + shadowOffsetY: 阴影垂直偏移，默认0；
     
- 绘制路径：
    + beginPath(): 开始一个新的路径。
    + closePath(): 闭合一个路径。
    + moveTo(): 路径绘制的起点。
    + lineTo(): 绘制直线到坐标点。
    + bezierCurveTo(): 绘制贝塞尔曲线到坐标。
    + quadraticCurveTo(): 绘制二次贝塞尔曲线到指定坐标。
    + arc(): 绘制圆弧
         param: (x, y, radius, startAngle, endAngle [, anticlockwise]) 顺逆时针。
    + arcTo: 给路径添加圆弧，需要控制点和半径。绘制的圆弧为正圆的一部分，绝不可能是椭圆的一部分。绘制圆弧，和之前的点以直线相连。
         param: (x1, y1, x2, y2, radius);
    + rect(): 绘制矩形路径。
    + ellipse(): 绘制椭圆路径。
    + clip(): 创建剪裁路径，之后绘制的路径只有在这里面，才会显示。
     
- 位置检测：
    + isPointInPath(): 当前点是否在指定路径内。 在路径上和在路径内，都为 true。
        * isPointInPath(x, y, fillRule, path)
        * 被检查点的x,y 坐标。
        * fillRule: nonzero默认(非零规则) | evenodd(奇偶规则);
            - nonzero: 顺时针逆时针数量，顺 +1, 逆 -1。 最终不为 0 则填充。在我看来，应该是点出现的次数吧。。
            - evenodd: 交叉路径数量。奇数为路径内，偶数为路径外。在我看来，应该重叠次数吧。重叠偶数次不显示，重叠奇数次填充。
        * 指 path2D 对象。
    + isPointInStroke(): 当前点是否在路径描边上。
     
- 变换：
    + rotate(): 旋转。
    + scale(): 缩放。
    + translate(): 位移。
    + transform(): 当前矩阵变换基础上再次矩阵变换。
    + setTransform(): 直接重置为当前设置的矩阵变换。
     
- 透明度和层级：
    + globalAlpha: 全局透明度。
    + globalCompositeOperation:设置图形叠加时候的混合方式，可以用来改变绘制元素上下叠加关系，也就是层级。
    + 作用： 可以衍生许多效果: 遮罩，剪裁。
    + source-over：直接在现有图形的上方绘制，纯视觉覆盖，
    + source-in：
    + source-out：
    + source-atop：
    + destination-over：
    + destination-in：
    + destination-out：
    + destination-atop：
    + lighter:
    + copy:
    + xor:
    + multiply:
    + screen:
    + overlay:
    + darken
    + lighten:
    + color-dodge
    + color-burn
    + hard-light
    + soft-light
    + difference
    + exclusion
    + hue
    + saturation
    + color
    + luminosity
     
- 图片与像素：
    + drawImage(): 图片绘制在画布上。
        * 作用： 对于很多图像的相关处理，如图像压缩，水印合成，像素操作。
        * drawImage(img, dx, dy, dwidth, dheight, sx, sy, swidth, sheight)
    + createImageData(): 创建一个新的空白的 ImageData 对象。
        * createImageData(width, height, imageData)
    + getImageData(): 获取 Canvas 画布设定区域的 ImageData 对象。中包含Canvas画布部分或完整的像素点信息。
        * getImageData(sx, sy, sWidth, sHeight);
    + putImageData(): 给定的 ImageData 对象应用在 Canvas 画布上。
        * putImageData(imageData, dx, dy, dirtyX, dirtyY, dirtyWidth, dirtyHeight)
     
- Canvas 状态:
    + save(): 保存当前Canvas画布状态并放在栈的最上面，可以使用restore()方法依次取出。
        * 作用：绘图效果本身不会被报错，只会保存绘图状态，如矩阵，裁剪，linestyle等状态信息。
        * 无参数，无返回值。
    + restore(): 依次从堆栈上方弹出存储的 canvas 状态，如果没有存储，则此方法无效果。
        * 无参数，无返回值。
    + canvas: 反向识别当前上下文的 HTMLCanvasElement.
        * 返回 canvas 元素。
     
- 其他方法：
    + drawFocusIfNeeded():可以让当前路径或者指定路径轮廓高亮，如果指定元素处于focus状态。
    + scrollPathIntoView(): 将当前路径或给定路径滚动到视图中。
