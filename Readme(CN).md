# 一个关于 DOM 绘制逻辑的 demo

## 使用说明

- 下载 index.html，使用浏览器打开；
- 蓝色方框是 DOM 的 border ， 两条黑色线条是在 Canvas 上绘制的；
- 使用 Ctrl + 鼠标滚轮的方式缩放页面，观察 DOM 的左上角是否与 Canvas 的线条完全对齐；

## 参数说明

### myCanvas
#### 构造函数
`id`: string，DOM 节点 id；     
`parent`: HTMLElement，父节点。
`top`: number，CSS 属性 top；   
`left`: number，CSS 属性 left；     
`height`: number，CSS 属性 height；     
`width`: number，CSS 属性 width；
#### drawLineOnCanvas()
`top`: number，线条起始点相对于 canvas 上边的距离；    
`left`: number，线条起始点相对于 canvas 左边的距离；   
`length`: number，线条长度；  
`weight`: number，线条宽度；  
`color`: string，线条颜色；   
`horizontal`: boolean，true 表示线条水平， false表示线条垂直；     
`isNew`: boolean，默认为 true，用于区分新绘制和缩放导致的重绘。

### myDom
#### 构造函数
`type`: string，DOM 节点的类型；   
`id`: string，DOM 节点 id；     
`parent`: HTMLElement，父节点。  
`top`: number，CSS 属性 top；   
`left`: number，CSS 属性 left；     
`height`: number，CSS 属性 height；     
`width`: number，CSS 属性 width；   
`border-width`: number，DOM 节点的边框宽度，不受缩放影响；  
`align`: boolean，true 表示对齐到格线外侧，false 表示对齐到格线内侧；   
`canvasLineWidth`: number，需要对齐到 Canvas 的线条的宽度，默认 1px；

[原理说明](https://kdocs.cn/l/covkZSNQCorN)
