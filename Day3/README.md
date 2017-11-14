# Selector - Child, descendants
[More to read](https://css-tricks.com/child-and-sibling-selectors/)

- Child combinator :
```css
ul li{background:red;} /*select all the child li element, even the nested one*/
ul>li{background:red;} /*select the child li element just one level down. Not the nested one.*/
```
- Adjacent sibling combinator :
The plus sign (+) is the adjacent sibling combinator. 选择他身边的那个，只有一个，如果后边还有一个一样的，就不选，但不包括他本身。
```css
/*it select the p next to the img element, but the img is not included, if there is another p after the p element, the second p is not selected.*/
img + p {
  margin: 0;
  font-style: italic;
}
```
- General sibling combinator : similar to adjacent sibling combinator, 但是他不止选身边的那个，是个sibling他都选。
```html
<div>
  <p>111</p>
  <p>222</p>
  <div id="part1">div in section 1</div>
  <p>333</p> //red color, green color
</div>
<div>
  <p>1</p>
  <p>2</p>
  <div>2 part</div>
  <p>4</p> //red color, green color
  <p>3</p> //red color
</div>
<p>outside</p> //red color, green color
```
```css
div ~ p{
  color:red;
}
div + p{
  color:green;
}
```
## clip-path
clip some part of the img out, and hide the other parts.
- clip-path: rectangle(x, y, width, height, rounded-x, rounded-y)
- clip-path: inset-rectangle(from top, from right, from bottom, from left, rounded-x, rounded-y)
- clip-path: polygon(a, bunch, of, points)
- clip-path: circle(radius at x, y)
- clip-path: ellipse(radius-x, radius-y at x, y)
