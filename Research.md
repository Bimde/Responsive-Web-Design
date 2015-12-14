#Responsive vs. Fluid Web Design
###Responsive Design (has multiple set viewport widths) 
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
* Must download all elements required for all viewports (performs worse) [1](http://studio.uxpin.com/blog/responsive-vs-adaptive-design-whats-best-choice-designers/)
  *Potential work arounds using media queries
* Must test every possible width to ensure no user has poor experience
* Content must either be able to be:
  * Cropped (i.e. [ykr portal fluid design demo](http://ykr-dev-portal4.devyork.ca:10039/wps/portal/ctcdemo/About/!ut/p/z1/tZNdb4IwFIb_CrvgkvTUAuIlLtmcEbKp27Q3pkDBTlsQq3H79ZbEZLsRZ-Z61eY85z0fzYsomiGq2F4UTItSsbV5z6m_mAC4_T4O4bEPGJ56OH6IvQgTH9B7G-C9-IieD4-Ih94QRTRVutJLNE91amVcljZ835al5DZUdVnUTNqQ8a0olKVrlq4MVirNlbZht-W1xQ8VrwVXKbdOWL5TGZOGYOttU6hKRWbKBFng4Zw5uJsRx-32sJPwJHACxpIM93yPu7h9sKZz-ofFNECTD2dO2OTTthLu2D8BLRqtCh4hFwDze3MzRfcHMJwSAzz7UTQGAhijyZVrbRccdG4tCDcWxLfuEJOrBYeXTGVc26mj-6gwskwvHaHyEs1-4xGTKT42GxoaUzbeOmg0-19XVvJVBuRTOKvx4GuaS7mIY4clARBvvR-Fd0eCOGcV/dz/d5/L2dBISEvZ0FBIS9nQSEh/))
  * or resized (ex. [Expression Engine's site](https://ellislab.com/expressionengine))
    * The header gets cut off but the content below scales on window resize 
* Can't make adjustments to specific viewports

####Examples
* [Graphics heavy demo](http://hoovermason.com/#/)
  * Has mostly fluid design with one jump
  * On the bigger jump, only the left side is fluid (the image gets cut off), allowing for the right side to have content that can not get cut off, i.e. the author’s picture 
* [Text adaptation example](http://www.highresolution.info/webdesign/sandbox/yaml_grids.html)
  * Shows some design challenges when moving text

###Analysis
####Content Creators
* Fluid - Restrictions on content, but faster to produce
  * Must create images capable of being cropped / resized
  * Can't control how exactly image will look for a specific device 
* Responsive - Control of output + flexibility when designing
  * Must create multiple versions of each image in orer to suit each viewport

####Developers
* Fluid - Less maintainance required, but harder to set up
  * Must test images / text scale nicely to any resolution with new pages / content
    * Limit flow of text / size of images to improve user experience, i.e. preventing text from taking up the enitre width of a widescreen monitor
  * Must create layout with good UX for mobile, but enough functionality for desktop
    * Must make decision between image cropping vs. image scaling / resizing
  * Must adjust layout with all possible viewports in mind
* Responsive - Straight-forward to set up, but harder to expand
  * Must tweak layout for each viewport with new pages
  * Must make sure new resolutions will render page properly, i.e. prevent a new mobile phone resolution / aspect ratio from displaying white bars along the sides
