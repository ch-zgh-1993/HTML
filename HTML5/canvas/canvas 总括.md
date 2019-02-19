/*
* @Author: Zhang Guohua
* @Date:   2019-02-12 17:22:11
* @Last Modified by:   zgh
* @Last Modified time: 2019-02-19 11:27:19
* @Description: create by zgh
* @GitHub: Savour Humor
*/
# Canvas


## 内容总括

### HTMLCanvasElement


### CanvasRenderingContext2D


### CanvasGradient
作用：表示 Canvas 的渐变对象。

由来： 可由CanvasRenderingContext2D.createLinearGradient()或者CanvasRenderingContext2D.createRadialGradient()这两个方法返回。

方法：

- addColorStop()： 增加新的渐变点。

### ImageBitmap
作用： 表示一个位图图像，可以将其绘制到 canvas 而不会产生不适当的延迟。

由来： createImageBitmap() 创建。

属性：

height: 
width:

方法：

close: 

### ImageData 

表示 cnavas 元素指定区域的像素信息。

由来： 可由CanvasRenderingContext2D对象中的createImageData()和getImageData()方法返回。

属性：

data:
height:
widht:


### TextMetries
表示 canvas 元素中的文本的尺寸。

由来： 由CanvasRenderingContext2D对象中的measureText()方法返回。

属性：

- width: 


### CanvasImageSource
不是真实存在的，代指所有可以作为 canvas 画布图片资源的统称。

包括：

- HTMLImageElement: img 元素，可以是dom,也可以是 Image 对象。
- SvgImageElement： svg 中的 image 元素。
- HTMLVideoElment: video 元素。
- HTMLCanvasElement: 
- imageBitmap:
- OffscreenCanvas： 屏幕外渲染的 Canvas 画布，可以在 window 和 worker 中拿到。

### CanvasPattern
表示 canvas 中的图案对象。

由来： CanvasRenderingContext2D.createPattern()这个方法返回。

### RenderingContext
统称，不是真实的接口：

内容：

- CanvasRenderingContext2D
- WebGLRenderingContext
- WebGL2RenderingContext

## 全局操作

- 清空画布： 清空绘制内容， 通过 bg.clearRect 清除，实际是将区域变为透明。下次使用 bg.fill 扔会展示出来。 canvas 每当宽，高重新设置时，会自动清空画布内容。