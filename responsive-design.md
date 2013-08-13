#Responsive Design: Three case studies

There's a lot more to responsive design than just changing the width of the page. These case studies document how three different sites were rebuilt to be responsive, and share ideas on 

##[Responsive News](http://responsivenews.co.uk/)
[Responsive News](http://responsivenews.co.uk/) is a blog written by the BBC News developers and covers a wide range of topics they came across while rebuilding the BBC News site. The BBC is especially interesting since the site needs to work in eleventy billion different browsers, most of which are rather old.

The key points this blog covers is '[cutting the mustard](http://responsivenews.co.uk/post/18948466399/cutting-the-mustard)' - a technique used to work out whether the browser is modern enough to have all the fancy new features, or an older one which should be served a basic (but accessible) version of the site.

The post on [responsive images](http://responsivenews.co.uk/post/50092458307/images) (every image has eighteen different versions!) is also good, but you should read every post on the site!

##[The Guardian mobile site](http://mattandrews.info/talks/port80-2013/)
This is from [a talk by Matt Andrews](http://mattandrews.info/talks/port80-2013/) (a front-end developer at the Guardian) at [Port 80](http://port80events.co.uk/) earlier this year. Similar to the BBC site, only the mobile site was rebuilt to be responsive - it's a huge job to rebuild the entire site, so most sites choose to rebuild only a section at a time.

This talk specifically mentions the BBC News approach, and covers which ideas were useful and which were expanded upon in rebuilding the Guardian. As with the BBC site, the Guardian checks [whether or not the browser can use certain features](http://mattandrews.info/talks/port80-2013/#/12), which then changes the version of the site shown to visitors.

[Images are dealt with in an interesting way](http://mattandrews.info/talks/port80-2013/#/22) (responsive images are always interesting because no-one's really worked out a good way to handle them yet) - the Guardian site always downloads a very small (140px wide) image initially, then checks to see if the browser is on a larger screen and downloads a bigger version.

The key thing from this talk was that [responsive design is about more than screen width](http://mattandrews.info/talks/port80-2013/#/29) - the speed of the connection should also be taken into account when deciding what to show users. For instance, a phone being used over Wifi can probably handle large images and web fonts, whereas a laptop being used on a train is likely to have quite a bad connection and so should be served only the core site content.

##[Boston Globe](http://upstatement.com/blog/2012/01/how-to-approach-a-responsive-design/)
The Boston Globe case study is a comprehensive look at the responsive redesign of the Boston Globe site, from the initial design phase to building the site. 

A lot of changes from the original designs were needed in different versions of the site depending on the width of the site - not everything could fit on the screen at once, so the developers had to consider what the most important items were and which could be hidden without affecting the user experience. The way the main site navigation changes depending on the screen size is a really interesting example of prioritising information on the screen.

This case study is also interesting since they went against the trend of designing for mobiles first. Instead, the designs started with the 960px version which had the most complex layout - lots of columns of information and with everything displayed.

##Overall
###Core experience

At smaller sizes not everything can fit onto the screen. Similarly, slower connections shouldn't be made to download extra 'nice-to-have' features such as web fonts or large images - you should consider what the core features of your site are (i.e. the content!) and make sure this is loaded first so that users aren't negatively affected by the size of their device or speed of connection.

###Screen size isn't the defining factor
Take into account the speed of the connection before serving large images or web fonts - just because a device has a large screen, it doesn't mean that it will have a fast internet connection.

Also consider whether browsers can handle certain features; if browsers can handle things natively, use them! Forcing users to download polyfills to fix issues in browsers they aren't even using is bad, and slows the site down for everyone.

###Multiple experiences (i.e. progressive enhancement)
It's ok for the same site to look different on different browsers. You can't make a site look identical on desktop and on mobile, so focus on creating the optimum experience for each one rather than having one all-round average version.

Since sites don't look the same on mobile and desktop, it's an easier conversation to have with the client to explain that the site doesn't have to be pixel perfect in every browser. As above, it is possible to make the site look exactly the same in ancient browsers, but this comes at the cost of making the site large and therefore slower (and also making your code a mess!)

###Images are a pain!
There are [many](http://css-tricks.com/which-responsive-images-solution-should-you-use/) [options](http://mobile.smashingmagazine.com/2013/07/08/choosing-a-responsive-image-solution/) for providing [responsive images](https://www.google.co.uk/search?q=responsive+images); currently there isn't a best-practice option. You'll have to weigh up the positives and negatives of each option and work out which will work best for your site.