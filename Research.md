#Adaptive vs. Fluid Web Design
###Adaptive Design (has multiple set viewport widths) 
####Pros
* Allows for mobile obtimization
  * Show specific content tailored to mobile users (ex. 'download our app')
* Easy to test / adapt
    * Only have to test content for 3 - 6 viewports
    * Adjustments made to specific viewports won't affect others

####Cons
* Harder to maintain content as new screen resolutions and form factors continue to come out
* Requires mulitple layouts / multiple versions of content

####Examples
* [York Region site](http://york.ca)
* [VML](http://www.vml.com/)

###Fluid Design  (adjusts to any screen size)

####Pros
* Adapts to any form factor
* Only create one version of content

####Cons
* User's will download all elements required for all viewports (**performs worse**)
  * [Comparison](http://studio.uxpin.com/blog/responsive-vs-adaptive-design-whats-best-choice-designers/)
  * [Specific problems](http://www.bypeople.com/responsive-design-problems/) (see section 11)
  * Potential work arounds using media queries
* Must test every possible width to ensure no user has poor experience
* Content must either be able to be:
  * Cropped (i.e. [ykr portal fluid design demo](http://ykr-dev-portal4.devyork.ca:10039/wps/portal/ctcdemo/About/!ut/p/z1/tZNdb4IwFIb_CrvgkvTUAuIlLtmcEbKp27Q3pkDBTlsQq3H79ZbEZLsRZ-Z61eY85z0fzYsomiGq2F4UTItSsbV5z6m_mAC4_T4O4bEPGJ56OH6IvQgTH9B7G-C9-IieD4-Ih94QRTRVutJLNE91amVcljZ835al5DZUdVnUTNqQ8a0olKVrlq4MVirNlbZht-W1xQ8VrwVXKbdOWL5TGZOGYOttU6hKRWbKBFng4Zw5uJsRx-32sJPwJHACxpIM93yPu7h9sKZz-ofFNECTD2dO2OTTthLu2D8BLRqtCh4hFwDze3MzRfcHMJwSAzz7UTQGAhijyZVrbRccdG4tCDcWxLfuEJOrBYeXTGVc26mj-6gwskwvHaHyEs1-4xGTKT42GxoaUzbeOmg0-19XVvJVBuRTOKvx4GuaS7mIY4clARBvvR-Fd0eCOGcV/dz/d5/L2dBISEvZ0FBIS9nQSEh/))
  * or resized (ex. [Expression Engine's site](https://ellislab.com/expressionengine))
    * The header gets cut off but the content below scales on window resize 
* Can't make adjustments to specific viewports without affecing others

####Examples
* [Graphics heavy demo](http://hoovermason.com/#/)
  * Has mostly fluid design with one jump
  * On the bigger jump, only the left side is fluid (the image gets cut off), allowing for the right side to have content that can not get cut off, i.e. the author’s picture 
* [Text adaptation example](http://www.highresolution.info/webdesign/sandbox/yaml_grids.html)
  * Shows some design challenges when moving text
* [Example](http://upstatement.com/) with consistent image resizing

###Analysis
####Content Creators
* Fluid - Restrictions on content, but faster to produce
  * Must create images capable of being cropped / resized
  * Can't control how exactly image will look for a specific device 
* Adaptive - Control of output + flexibility when designing
  * Must create multiple versions of each image in orer to suit each viewport

####Developers
* Fluid - Less maintainance required, but harder to set up
  * Must test images / text scale nicely to any resolution with new pages / content
    * Limit flow of text / size of images to improve user experience, i.e. preventing text from taking up the enitre width of a widescreen monitor
  * Must create layout with good UX for mobile, but enough functionality for desktop
    * Must make decision between image cropping vs. image scaling / resizing
  * Must make any adjustments to layout with all possible viewports in mind
* Responsive - Straight-forward to set up, but harder to expand
  * Must tweak layout for each viewport with new pages
  * Must make sure new resolutions will render page properly, i.e. prevent a new mobile phone resolution / aspect ratio from displaying white bars along the sides

###Solutions
* Using a mix of both layouts, as suggested by various outlets. Implementations include:
  * Google's '[Mostly fluid](https://developers.google.com/web/fundamentals/design-and-ui/responsive/patterns/mostly-fluid?hl=en)' design
  * [Boston Globe's approach](http://upstatement.com/blog/2012/01/how-to-approach-a-responsive-design/)
* [My example](https://b6ed4c3b83435ede471472942e6392f1667cc0d2.googledrive.com/host/0B8Lpd3aKTxDRYlYzVW5nZkdFNlU/) (using a combination of both fluid and responsive design)
  * Images scale on window resize without getting cropped (both the header and the image in the paragraph)
  * Sidebar moves to bottom when window width is less than 600px
  * View the code [here](https://github.com/Bimde/Responsive-Web-Design/blob/master/Responsive%20%2B%20Fluid%20Web%20Design.html)
