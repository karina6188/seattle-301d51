Article: Responsive Web Design

Responsive web design is the practice of building a website suitable to work on every device and every screen size, no matter mobile or desktop.

Responsive vs. Adaptive vs. Mobile
	• Responsive generally means to react quickly and positively to any change. This means responsive design websites continually and fluidly change based on different factors.
	• Adaptive means to be easily modified for a new purpose or situation. Adaptive websites are built to a group of preset factors.
	• Mobile generally means to build a separate website commonly on a new domain solely for mobile users.

Three main components of responsive web design: flexible layouts, media queries, flexible media.

Flexible Layouts: building the layout of a website with a flexible grid, which has the capability to dynamically resize any length or width. Flexible grids are built using relative length units, like percentages or em units.

Take the target width of an element and dividing it by the width of its parent element.
target / context = result   (target width / parent width = desired relative width)

It's better to set min/max width and height because even we can use the relative sizing to change elements to the correct proportions, when the layout gets too small or too large, the contents may not be legible to be displayed or the layout will break.

P.S.   CSS3 Relative Viewport Lengths:
	• vw: viewports width
	• vh: viewports height
	• vmin: minimum viewport height and width
	• vmax: maximum viewport height and width
	
Media Queries: 
Media queries provide the ability to specify different styles for individual browser and device circumstances. Media queries may include media type to specify different circumstances. Media types may include media features and values that can be allocated to be true or false. When it is allocated to be true, the styles are applied. When it's false, the styles are ignored.

Logical operators: and, not, only. These are used within media queries to allow some additional conditions.

Media Features: Media features identify what attributes or properties will be targeted within the media query expression.
ex. @media all and (min-width: 320px) and (max-width: 780px) {...}  These are media features; these are values

Media features:
	• Height and Width
	• Orientation   ex. landscape or portrait
	• Aspect Ratio   ex. @media all and (min-device-aspect-ratio: 16/9) {...}
	• Resolution   ex. @media print and (min-resolution: 300dpi) {...}
	• Color   ex. color, color-index, or monochrome (black and white)

P.S.   Responsive website should adjust to an array of different viewport sizes instead of devices. Since new devices and resolutions are being released all the time, it will be difficult to keep up with the changes.

Mobile First:
This is an approach to use styles targeted at smaller viewports as the default, then use media queries to add styles when viewport changes. This eliminating the load of styles for a desktop computer only to have them over written with mobile styles later.

When use media queries to style mobile devices, avoid CSS3 shadows, gradients, transforms, and animations to prevent heavy loading the media assets to reduce device's battery life.

Viewport meta tag are commonly used to set styles of how a website should be rendered, it has been made to be a CSS @rule, which is @viewport.

Flexible Media: 
Images, videos, and other media types need to be scalable, changing their size as the size of the viewport changes.

Set media property max-width to be 100%, so when the viewport size changes, media types scales up and down according to its containers width. However, this is not suitable for embedded media (using iframe).

When resizing embedded media, set the embedded media to have absolute position and set the parent element to have relative position and width of 100%, so the embedded element changes according to viewport.



Article: All About Floats

Float is a CSS property that aligns elements to be on the left or right side within its container. This can also be done using absolute position to layout the elements to the position you want. However, when using absolute positioning, the other elements around it is not affected when you resize the element.

Similar to float, clear is used to align elements by specifying which side of the element does not touch other elements.

Other ways to clear floats including empty div method, overflow method, and easy clearing method.
	1) Empty div method: an empty div goes across the whole width of the browser to create space for floating elements.
	2) Overflow method: set the property to auto or hidden on the parent element, then the parent expands to contain the floats, which effectively clears it for succeeding elements.
  3) Easy clearing method: this method uses CSS pseudo selector :after to clear floats.