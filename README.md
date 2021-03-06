HelpBubbles.js
==============

This class pops up "Bubbles" with a title and an explanation next to the defined elements. 
Following the concept of convention over configuration if you're using the default values using this class is as easy as including the .js and .css file (after mootools), adding the two custom attributes (data-anchor-title and data-anchor-text) to the elements you want the help associated, with the information you want to display and adding the class triggerHelp to the button, link or whatever you want to start showing the bubbles.

Dependencies
------------
You need Mootools core (only tested with 1.3.1) and some packages from the More. All included in the repo.
More dependencies:
- Fx.Move
- Element.Position

Usage
-----

Add the following into your header:
	<script type="text/javascript" src="mootools/mootools-core-1.3.js"></script> // or your existing mootools library, only tested in Mootools 1.3
	<script type="text/javascript" src="mootools/mootools-more.js"></script> // or your existing library remember to include Fx.Move and Element.Position
	<script type="text/javascript" src="helpBubble.js"></script>

Add the css:
	<link rel="stylesheet" href="style.css" type="text/css" media="all" /> // Or your own

You instantiate the class like this:
	<script type="text/javascript">
		popup = new HelpBubble;
	</script>

You need to set a trigger: 
(it may be a link or a button or anything, just something with the class 'triggerHelp'or you pass the class you want as an option)
<button class="triggerHelp">Help Here! Click Me!</button>

You're all set. Just add the attributes data-anchor-title to set the title of the bubble and data-anchor-text for the text or (simple) html inside.
<div data-anchor-title="Title 1" data-anchor-text="This is the first paragraph or Lorem Ipsum"></div>
<div data-anchor-title="Title 2" data-anchor-text="This is the second paragraph or Lorem Ipsum"></div>

Options
-------
	<script type="text/javascript">
		popup = new HelpBubble({
			// options
		});
	</script>

	Options List:
		anchorTitle: 
			default = 'data-anchor-title'
			Defines the attribute to look for the bubble title
		
		anchorText: 
			default = 'data-anchor-text'
			Defines the attribute to look for the bubble text
			
		popupContainerClass: 
			default = 'Bubble'
			Defines the class of the container bubble

		popupContainerId: 
			default = 'BubbleId'
			Defines the id of the container bubble

		popupClassTop: 
			default = 'Btop'
			Defines the class to assign to the bubble container when the bubble is on top of the element
		popupClassBottom: 
			default = 'Bbottom'
			Defines the class to assign to the bubble container when the bubble is under the element
		popupClassLeft: 
			default = 'Bleft'
			Defines the class to assign to the bubble container when the bubble is to the left of the element
		popupClassRight: 
			default = 'Bright'
			Defines the class to assign to the bubble container when the bubble is to the right of the element
		popupClassClose: 
			default = 'Bclose'
			Defines the class to assign to the close bubble link
		popupCloseText: 
			default = 'X'
			Defines the text/image to assign to the close bubble link
		popupClassContent: 
			default = 'Bcontent'
			Defines the class of the content container of the bubble
		popupClassTip: 
			default = 'Btip'
			Defines the class of the tip of the bubble
		triggerClass: 
			default = 'triggerHelp'
			Defines the class of the element that will trigger the show bubble event
		hasNavigation: 
			default = true
			If true will show the next and previous links
		navigationWrapperClass: 
			default = 'Boptions'
			Defines the class of the container for the bubble navigation
		nextTriggerId: 
			default = 'help-trigger-next'
			Defines the id of the navigation next link
		nextTriggerText: 
			default = 'Next'
			Defines the text of the navigation next link
		nextTriggerClass: 
			default = 'Bnext'
			Defines the class of the navigation next link
		prevTriggerId: 
			default = 'help-trigger-prev'
			Defines the id of the navigation previous link
		prevTriggerText: 
			default = 'Prev'
			Defines the text of the navigation previous link
		prevTriggerClass: 
			default = 'Bprev'
			Defines the class of the navigation previous link
		titleAttribute: 
			default = 'strong'
			Defines the attribute to wrap the bubble's title
		titleClass: 
			default = 'Btitle'
			Defines the class of the bubble's title
		textAttribute: 
			default = 'p'
			Defines the attribute to wrap the bubble's text
		textClass: 
			default = 'Btext'
			Defines the class of the bubble's text
		leftMargin: 
			default = 200
			This sets the left margin, if the right edge of the element the bubble will be assigned to is < this limit, the bubble will not display to the left of this element.
		rightMargin: 
			default = 200
			This sets the right margin, if the left edge of the element the bubble will be assigned to is between this limit and the edge of the page, the bubble will not display to the right of this element.
		topMargin: 
			default = 450
			This sets the top margin, if the top edge of the element the bubble will be assigned to is < this limit, the bubble will not display on top of this element.
		bottomMargin: 
			default = 400,
			This sets the bottom margin, if the bottom edge of the element the bubble will be assigned to is between this limit and the edge of the page, the bubble will not display under this element.
		offset: 
			default = 10
			This sets the distance between the element and the help bubble


License
-------

Copyright (c) 2011 - Juan Andrés Peón <juan.peon@replayful.com> Máximo Gómez <maximo.gomez@replayful.com>

Permission is hereby granted, free of charge, to any
person obtaining a copy of this software and associated
documentation files (the "Software"), to deal in the
Software without restriction, including without limitation
the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the
Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice
shall be included in all copies or substantial portions of
the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY
KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE
WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR
PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS
OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR
OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR
OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

Credits
-------

Thanks to Replayful, which gives us awesome things to work on

