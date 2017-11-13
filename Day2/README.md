# Animation of Nav icon
Turn a hamburger icon into a cross icon on click.

## Transform
`transform`: 变型，是2d或3d的空间变形。It allows to change an element by skew(倾斜), rotate（旋转）, translate（移位）, or scale（缩放）.
- translate: `translate(x,y)`, 以x,y轴进行移动。translate可以和top，left配合使用来center一个block.
```css
myBlock{
  top:50%;
  left:50%;
  transform: translate(-50%, -50%);
  width:20px;
  height:20px;
  position：absolute；/*zhe ge bi xu you*/
}
```
- rotate : `rotate(angle)`. 以中心点进行旋转。
- scale : `scale(x,y)`. 以中心点进行缩放。
- skew : `skew(x-angle,y-angle)`. 以中心点进行扭曲的变形。

## Transition
`transition` : 用来从一个状态过渡变到另一个状态的，是时间上的。他只是以下四个property的缩写而已，木有什么主要意义。
- `transition-property`：要改变状态的css属性名称，就是要在什么东西上进行改变
- `transition-duration`：一共需要多少时间
- `transition-timing-function`：效果 ease, linear, cubic-bezier(自定义)
- `transition-delay`：几秒钟后开始行动

#### Note：
1. Transition是必须有事件触发的，不会自动在page loading的时候启动。
2. 它是一次性的，除非重新触发，否则不能重复发生。
3. 没有中间状态，只有开始和结束状态。
4. 一条规则，只能定义一个属性的变化，不能涉及多个属性。[阮一峰CSS简介](http://www.ruanyifeng.com/blog/2014/02/css_transition_and_animation.html)

**所以，才出现了Animation，来解决这个问题。**

## Animation
`animation` 要有一个动画效果的名字，这个是名字的内容是由`@keyframes`决定的。这个可以弥补transition不能有中间状态的缺陷. It also need a duration time, and iteration count.
```css
.element{
  animation : line-1-nor 1s infinite;
 }
 @keyframes line-1-nor{
  0%{ background:red;}
  50%{background:green;}
  100%{background:blue;}
 }
 ```
 other properties :
 - animation-fill-mode: forwards表示让动画停留在结束状态
 - animation-direction: sets the direction of the animation after the cycle. normal, alternate, reverse
 - animation-play-state:  pause/running
 
