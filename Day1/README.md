# Day1 Challenge
Create a block with some words.

## Box Shadow
`box-shadow: [horizontal offset] [vertical offset] [blur radius] [optional spread radius] [color];`
- horizontal offset : positive means the shadow will be on the right of the box, a negative offset will put the shadow on 
the left of the box.
- vertical offset : positive one means the shadow will be below the box, negative one means the box-shadow will be above the box
- blur radius: 0 the shadow will be sharp, the higher the number, the more blurred it will be
- spread radius : positive values increase the size of the shadow, negative values decrease the size.
- inset : changes the shadow to one inside the frame (as if the content was depressed inside the box).
```css
.shadow {
   box-shadow: inset 0 0 10px #000000;
}
```
[More to read](https://css-tricks.com/almanac/properties/b/box-shadow/) 

## Relative parent with its absolute children.

A page element with relative positioning gives you the control to absolutely position children elements inside of it. It is 
no longer absolute to the window, but absolute to their parent. 

[More to read](https://css-tricks.com/absolute-positioning-inside-relative-positioning/)

## Gradient
`linear-gradient` and `radial-gradient`
`background: linear-gradient(direction/angle, color-stop1, color-stop2, ...);`

## text-transform
Control the text case and capitalization. It apply to **all the letters or every word**
- lowercase: makes **all selected** letters in lowercase.
- uppercase: makes **all selected** letters in uppercase.
- capitalize: makes **every selected** word's first letter capitalized.
```css
.cap{
  text-transform: capitalize;
}/*Every Word Is Capitalized.*/
```
If just need to capitalize the first letter of a paragrahp, use `::first-letter`
```css
p::first-letter {
  font-weight: bold;
  color: red;
}
/*The first letter is bold and red*/
```
