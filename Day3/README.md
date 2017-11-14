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
/*it select the p next to the img element, but the img is not included, if there is another p after the p element, the second p is not
selected.*/
img + p {
  margin: 0;
  font-style: italic;
}
```
- General sibling combinator : 
