body {

​	font-family: Helvetica;

}

## Position of elements

* Normal flow (*default*)
	* position:static
* Relative positioning
	* pisition:relative  
Relative positioning moves an element in relation where it would have been in normal flow.
* Absolute positioning
	* position:absolute  
When the position property is given a value of absolute, the box is taken out of normal flow and no longer affects the position of other elements on the page.(They act like it is not there.)  
* Fixed positioning
	* position:fixed  
Fixed positioning is a type of absolute positioning that requires the position property to have a value of fixed.
* Overlapping elements
	* z-index  
When you use relative, fixed, or absolute positioning, boxes can overlap. If boxes fo overlap, the elements that appear later in the HTML code sit on top of those that are earlier in the page.If you want to control which elements sits on top, you can use the z-index property.

## BOX

### Limiting width

* min-width

  The smallest size a box can be displayed at when the browser window is narrow.

* max-width

  The maximum width a box can stretch to when the browser window is wide.

  **Limiting height**: same as width.