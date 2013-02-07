scss_lightfoot
==============

scss_lightfoot - A quick and powerful grid system that employs scss to minimise 'tag soup'.

Requirements
------------

Sass	(http://sass-lang.com/)
Compass (http://compass-style.org/)
A Text Editor

Installation & Usage
--------------------

Currently, all the scss is located in the scss/_grid.scss file. It would be relatively easy to use the @import function on a existing scss file. This setup has this already in place and the _grid.scss is imported into the screen.scss file.

The Grid works similar to the 960.gs grid and employs a fixed width container object and 12 grid sizes defined as 'blocks'. By default, a grid can be created using the Grid classes, which are labeled 01-12. The last block on the grid is defined by a suffix to the class name, ie .block12_last. An example would be:

	<div class="container">
		<div class="block05">
			<p>Content goes here</p>	
	</div>
		<div class="block07_last">
		</div>
	</div>

This would create a grid with two blocks, the first using 5 'grids' and the second using 7.

This works a lot like most grid systems, but I find it results in very ugly html. To improve the semantics of your code, I recommend using the @extend function found in Sass/Scss.

An example in your scss file would be:

	#blogContainer {
		@extend .block05;
	}

An example of your html would be:

	<div class="container">
		<div id="blogContainer">
			<p>Content goes here</p>	
		</div>
		<div class="block07_last">
		</div>
	</div>

It's that simple!

It's also responsive, currently it targets 4 resolutions, all of which is configrable in the _grid.scss file. You can adjust the container size and gutter size and the entire grid reacts automatically.

Bugs
----
- Responsiveness breaks (easy fix)
- Border variables 'half implimented' 

Changelog
---------
- 070213 - Intial Version Release

License
-------
This is released under the MIT Open Source Licence.

Copyright (c) 2013 David Henderson

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
