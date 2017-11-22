# Who is more important!
Specificity of css : !important > inline style> ID > Class/Attributes/pseudo-classes > Elements/ pseudo-elements, others have no
effect on Specificity.

## !important
it over writes everything, even the inline style.
```html
<style> p{ color:red !important; } </style>
<p style="color:blue;">Text</p>　
<!--the color should be red.-->

<style> p{ color:red !important; } </style>
<p style="color:blue; !important">Text</p>　
<!--Blue, because two !important is equal to none, then inlinestyle wins-->
```
## Calculate them
- inlineStyle : 1000
- ID : 0100 
- Class/attr/pseudo-class:0010 - `:hover,:target, :visited`
- elements/pseudo-elements: 0001  - element tags like `<p>,<h1>,<form>, :before, :first-child`
- others :0000  - :not()**[anything inside not() still count]**, *, =, +, ~

```css
* {color: blue}  /* 0000 */
p:last-child {color: blue}  /* 0001+0001 = 0002 */
ul ol+li {color: blue}  /* 0001(ul)+0001(li)+0001(ol)+0000(+) = 0003 */
ul + *[type="radio"] {color: blue}  /* 0001(ul)+0010([type="radio"])+0000(+,*) = 0011 */
ul ol li a.blue  {color: blue}  /* 0001(il)+0001(ul)+0001(ol)+0001(a)+0010(.blue) = 0014 */
#green {color: blue}  /* 0100 */
<p style="color: blue"></p> /* 1000*/

/*-----------------------昏割线---------------------------------------*/

body header div nav ul li div p a span em {color: red} /*0,0,0,11*/
.count {color: blue} /*0,0,1,0*/
/*color blue wins over red*/
```

- if the result of the cal ar the same, the last one appears in the css style wins.
```css
.parent .child {color: blue;}   /* 0,0,2,0 */
.parent :not(.p) {color: red;}  /* 0,0,2,0 */
/* color should be red, because it is the last one in the styles.*/
.parent .child {color: red;}   
.parent :not(.p) {color: blue;} 
/* swap them, it will be blue*/
```
