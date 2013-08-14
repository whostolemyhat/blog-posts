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
Don't want to serve huge images to phones; don't want 


examples
frameworks

http://johnpolacek.github.io/scrolldeck.js/decks/responsive/