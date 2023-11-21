# dom-canvas-alignment
A demo which illustrates a method to match the behavior of a DOM element to a grid drawn on a Canvas element when users zoom in or out in the browser. The method also took consideration of the occasionally appeared blurry edges when displaying a Canvas grid and address the issue accrodingly.

## How to Use

- Open index.html in any broser except Safari.
- Blue box is a DOM border, black grid is drawn on Canvas.
- Hold "Ctrl" and use scroll wheel on your mouse，observe DOM border's behavior.
- Modify certain paramters listed below, examine the method under different situations.

## Paramters

### myCanvas
#### constructor
`id`: string，id of the element；     
`parent`: HTMLElement，parent node；   
`top`: number，CSS attribute top；   
`left`: number，CSS attribute left；     
`height`: number，CSS attribute height；     
`width`: number，CSS attribute width；
#### drawLineOnCanvas()
`top`: number，y-coordinates of the starting point of a line；    
`left`: number，x-coordinates of the starting point of a line；   
`length`: number，length of the line；  
`weight`: number，width of the line；  
`color`: string，color of the line；   
`horizontal`: boolean，true for a horizontal line, false for a vertical line；     
`isNew`: boolean，default to true，used to indicate the update process when zoom happens；

### myDom
#### constructor
`type`: string，type of the DOM element；   
`id`: string，id of the element；     
`parent`: HTMLElement，parent node；     
`top`: number，CSS attribute top；   
`left`: number，CSS attribute left；     
`height`: number，CSS attribute height；     
`width`: number，CSS attribute width；   
`border-width`: number，border width of DOM element，unaffected by zoom；  
`align`: boolean，align to the outer box of the grid when set to true，otherwise align to the inner box；   
`canvasLineWidth`: number，width of grid lines on Canvas，defualted to 1px；
