#Responsive Design

#Difference between responsive and adaptive design
##responsive
Responsive design adapts the layout of websites to provide an optimal experience based on the device used to view the site.
One codebase
Fluid layout

##adaptive
Separate site which detects size or user-string
Predefined set of sizes

Both allow sites to be viewed in optimised version

##why?
Huge variety of devices and browsers; don't want to create a site for every different device size - can't predict form of popular devices in 5 years
Build iphone site;ipad site; dumbphone site etc
Reduce codebase/number of templates


#(Screen) Size isn't everything
Screen size is only one factor: internet speed, browser capability
Take into account the speed of the connection before serving large images or web fonts - just because a device has a large screen, it doesn't mean that it will have a fast internet connection.

Also consider whether browsers can handle certain features; if browsers can handle things natively, use them! Forcing users to download polyfills to fix issues in browsers they aren't even using is bad, and slows the site down for everyone.

Google now: location, time, recent searches, calendar events. http://paulstamatiou.com/android-is-better
http://www.google.com/landing/now/

#Mobile-first and progressive enhancement
Mobile-first = some browsers don't understand @media so serve the basic phone version first.
P.E. - similar to screen size; give content first then layer on better images/fonts/functionality if needed.

It's ok for the same site to look different on different browsers. You can't make a site look identical on desktop and on mobile, so focus on creating the optimum experience for each one rather than having one all-round average version.

Since sites don't look the same on mobile and desktop, it's an easier conversation to have with the client to explain that the site doesn't have to be pixel perfect in every browser. As above, it is possible to make the site look exactly the same in ancient browsers, but this comes at the cost of making the site large and therefore slower (and also making your code a mess!)


#Images
Many different versions
Don't want to serve huge images to phones
http://mobile.smashingmagazine.com/2013/08/21/webkit-implements-srcset-and-why-its-a-good-thing/


examples
frameworks

http://johnpolacek.github.io/scrolldeck.js/decks/responsive/

gov.uk
ethanmarcotte site


Things to cover off:
•	How does device influence each option
•	How does a fully responsive site work (with no breakpoints?)
•	Image optimisation
•	SEO
•	Future proof
•	Technical vs ID development overhead
•	Knowing what we know now, what would have been the best mobile approach for: BP, V Group, Premier Marinas, Sainsbury’s, 
•	Bring any other related discussion points 
•	How good can adaptive be for us to recommend it (based on cost/timeframes/scoping overheads)

HOMEWORK:
RESPONSIVE:
Positives
•	Allows for your website to render its layouts dimensions based on whatever viewing range is currently loading it is
•	When coded properly, everything will always look in balance and sync with everything else
•	Little worry necessary when something changes in the technology world that affects how people browse the web
•	Same Experience for Everyone - Mobile users will see a slightly different layout from desktop users, however by and large everyone viewing your site will get the same experience.
•	Less Maintenance - Multiple designs take more time to update. By using a single responsive design, you can reduce the time you spend updating your designs.
•	Everything is on One URL - Desktop, tablet and smartphone users will all view a page using the same URL. This is better for social media sharing and optimising search engine rankings. It also means that your stats will not be split up for different versions of your website.
•	It's Google Friendly - Google went on record at the end of last year stating that they prefer website owners to use responsive designs. They noted that: "Google can discover your content more efficiently as we wouldn't need to crawl a page with the different Googlebot user agents to retrieve and index all the content."
•	
Negatives
•	Much time must be spent looking at the website at different viewing widths to see where it breaks in the design
•	If coded poorly, there will easily noticeable inconsistencies in position, size, margins, etc.
•	It is not future proof, and requires periodic updates as technology changes
•	Website Performance – Loading times are the biggest concern of responsive designs. When someone loads a web page with a responsive design, they load the information for all devices, not just the one they are viewing your website on. Images are a concern too. Most designs simply scale down the size of an image. Therefore, smartphone users may download an image of 1,000 by 1,000 pixels in width, despite it being scaled down to 250 by 250 pixels on their device.
•	Integrating Advertisements – It is more difficult to integrate advertising effectively into a responsive design as ads have to fit nicely into all resolutions.
•	Sacrificing Functionality – A lot of sacrifices have to be made when using one single design for all devices. For example, you will have to compromise your reader’s desktop experience to ensure that the experience for mobile users is not hindered (and vice-versa).
•	
•	
Adaptive
Positives
•	Less of a need to test a website at the various widths to figure out how it will render
•	Ensures an optimal viewing experience for a good percentage of possible users
•	Has a set number of a few different layouts
•	Website Performance – Loading times are the biggest concern of responsive designs. When someone loads a web page with a responsive design, they load the information for all devices, not just the one they are viewing your website on. Images are a concern too. Most designs simply scale down the size of an image. Therefore, smartphone users may download an image of 1,000 by 1,000 pixels in width, despite it being scaled down to 250 by 250 pixels on their device.
•	Integrating Advertisements – It is more difficult to integrate advertising effectively into a responsive design as ads have to fit nicely into all resolutions.
•	Sacrificing Functionality – A lot of sacrifices have to be made when using one single design for all devices. For example, you will have to compromise your reader’s desktop experience to ensure that the experience for mobile users is not hindered (and vice-versa).
Negatives
•	In the specified ranges there will be a point where the design will have issues
•	Users who aren’t using the most popular devices have a high chance of a less than optimal experience
•	It is not future proof, and requires periodic updates as technology changes
•	Bad for Search Engines – Two different designs means that there each article/section has two separate URL’s. In the example given previously, the symptons section is located at www.breastcancer.org/symptoms on the full website and m.breastcancer.org/symptoms on the mobile website. Search engines do not like identical articles being on different URL’s, therefore your traffice may be reduced as a result of this (though I have not seen any case studies on this issue that verifies this).
•	Cross-Linking – Linking internally becomes difficult when you have more than one version of your website. Do you link to the full version or the mobile version of your article? You may have to set up redirects so that someone who clicks on the full article from the mobile design is redirected to the mobile version of the article.
•	Stuck in the Middle – Mobile users usually find the mobile-optimized version of a design to be easier to navigate, however tablet users may not. It really depends on the device. Tablets generally range from 5″ to “11 in size. Those with smaller screens may prefer the mobile version of your website whilst others will prefer viewing the full version of your design. BreastCancer.org did the right thing by adding a link in the footer of each design that allows the user to change what design they are viewing. However, this does not stop a user from landing on the wrong version in the first instance.
•	Some reading:
•	Explanation: http://www.searchenginepeople.com/blog/the-difference-between-adaptive-design-and-responsive-design.html
•	On the responsive corner: http://www.cmswire.com/cms/customer-experience/mobile-web-responsive-design-or-separate-mobile-site-app-021689.php
