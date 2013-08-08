#Parsing RSS feeds with jQuery

I recently came across this [jQuery snippet on Stack Overflow](http://stackoverflow.com/a/6271906/345078) which can be used to convert RSS feeds (which are almost always in XML format) into JSON, which can be used directly in Javascript.

    function parseRSS(url, callback) {
        $.ajax({
            url: document.location.protocol + '//ajax.googleapis.com/ajax/services/feed/load?v=1.0&num=10&callback=?&q=' + encodeURIComponent(url),
            dataType: 'json',
            success: function(data) {
            callback(data.responseData.feed);
            }
        });
    }
    
This function calls the RSS feed through Google's cache, which then returns the feed as JSON (which is much easier to use with Javascript, since it's just a Javascript object).

Since it's called through Google, it won't update immediately (Google needs to crawl the feed for new stories to appear).