# CSS

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

- min-width
	- The smallest size a box can be displayed at when the browser window is narrow.
- max-width
	- The maximum width a box can stretch to when the browser window is wide.
	- **Limiting height**: same as width. 

### Overflowing content

- **hidden: **This property simply hides any extra content that does not fit in the box.

	```html
	overflow: hidden
	```

- **scrol:** This property adds a scrollbar to the box so that users can scroll to see the missing content.

### Inline/Block

- Inline: This causes  a block-level element to act like an inline element.
- block: This causes an inline element to act like a block-level element.
- none: This hides an element from the page. **Not on the page**
- visibility: hidden. **On the page, black space**

###  Shadows

- box-show: 5px, 5px, 5px, 5px, #777777, inset  
	- horizontal
	- vertical
	- blur
	- spread
	- color
	- inner-shadow

### Rounded corners

- border-radius: 5px, 10px, 5px, 10px
	- border-top-right-radius
	- border-bottom-right-radius
	- border-bottom-left-radius
	- border-top-left-radius

* Elliptical shapes
	* border-radius: 100px **circle**
	* border-radius: 80px 50px **corner**

## List

### Bullet point style

* list-style-type
	* unordered lists
		* none ( )
		* disc (●)
		* circle (○)
		* square ( ◼︎)
	* order lists
		* decimal (1 2 3)
		* decimal-leading-zero (01 02 03)
		* lower-alpha (a b c)
		* upper-alpha (A B C)
		* lower-roman (i. ii. iii.)
		* upper-roman (I II III)
* list-style-image: url("…")

### Positioning the marker

* list-style-position
	* outside: The marker sits to the left of the box of text.
	* inside: The marker sits inside the box of the text.

### shorthand

* list-style: (position, style)

## Table

### Properties

* width
* padding
* text-transform: to convert the content of the table headers to uppercase.
* letter-spacing, font-size
* border-top, border-bottom
* text-align
* background-color
* :hove: to highlight a table row when a user's mouse goes over it

### Tips

* give cells padding
* distinguish headings
* shade alternate rows
* align numerals

### Cell

* empty-cells
	* show: shows the borders of any empty cells
	* hide: hides the borders of any empty cells
* border-spacing
	* controll the distance between adjacent cells.
* border-collapse
	* collapse: Borders are collapsed into a single border where possible.
	* separate:Borders are detached from each other.

## Forms

### Most common to style

* Text input and text areas
* Submit buttons
* Labels on forms, to get the form controls to align nicely

### Text input

* font-size
* color
* background-color
* background-repeat
* border
* border-radius
* **:focus**
	* change the background color of the text input when it is being used
* **:hover**
	* applies the same :focus styles when the user hovers over them
* background-image

❖ ***Transition***

* transition-property
	* Specifies the name of the CSS property the transition effect is for
* transition-duration
	* Specifies how many seconds or milliseconds the transition effect takes to complete
* transition-timing-funciton
	* Specifies the speed curve of the transition effect
* transition-delay
	* Defines when the transition effect will start
* initial
	* Sets this property to its default value
* inherit
	* Inherit this property from its parent element





