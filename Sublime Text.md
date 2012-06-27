#Sublime Text

##Really Useful Plugins

###Package Control
*[Package Control](http://wbond.net/sublime_packages/package_control) is a package manager for Sublime Text 2. It makes finding and installing plugins incredibly easy.*

The best plugin for Sublime Text 2 is the [Package Control](http://wbond.net/sublime_packages/package_control) plugin, which is absolutely essential. Package Control lists available plugins and also takes care of installing them, meaning plugin installation is as simple as typing part of a package name (to see what's available) and choosing from a list. [example]

For example, if you wanted SASS syntax highlighting, you simply open the Command Pallete (Ctrl+Shift+P) and type 'Install' to find the installation command. This will then show you a list of available plugins; type 'SASS' to find SASS-related plugins, then choose an appropriate plugin and press 'Enter' to install. Plugins are even installed without having to restart Sublime Text!

Package Control can be installed by running the following command in the Sublime Text 2 console (opened with Ctrl+` (backtick) or View > Console):

`import urllib2,os; pf='Package Control.sublime-package'; ipp=sublime.installed_packages_path(); os.makedirs(ipp) if not os.path.exists(ipp) else None; urllib2.install_opener(urllib2.build_opener(urllib2.ProxyHandler())); open(os.path.join(ipp,pf),'wb').write(urllib2.urlopen('http://sublime.wbond.net/'+pf.replace(' ','%20')).read()); print 'Please restart Sublime Text to finish installation'`

The rest of the plugins mentioned here can all be installed through Package Control by pressing Ctrl+Shift+P to open the Command Pallete, then typing 'Install' to find the installation command as above.

###Zen Coding
*Zen Coding allows auto-completion of snippets by pressing tab.*

The Zen Coding plugin is installed by default in Sublime. This plugin makes creating HTML vastly quicker and easier - instead of typing out each tag and nesting them, you type a snippet version and press 'Tab' to expand it into HTML. For example, to create a list with an id of 'nav' containing three links, the Zen snippet would be: <pre>ul#nav>li*3>a</pre>
This expands to:

    <ul id="nav">
	    <li><a href=""></a></li>
		<li><a href=""></a></li>
		<li><a href=""></a></li>
    </ul>



[link]Zen Coding syntax

###Tag
*Tag provides a number of useful functions for working with markup, such as auto-closing tags and tidying up formatting.*

Tag is one of my favourite plugins when I'm working with HTML - not only does it highlight tags which are missing closing tags, but it also inserts the correct closing tag when you type `</` (the start of a closing tag).

Another incredibly useful feature of Tag is it's format command - open the Command Pallete and type 'Format' to find the command (the document needs to be HTML syntax) and Tag will tidy up the formatting for you. While it doesn't always lay out tags in the way I would, it's still infintely faster than trying to clean up formatting by hand.

##Other Plugins
*Other plugins which I've found useful* 
###BracketHighlighter
*Matches pairs of brackets*

###WordHighlighter
*Matches all occurences of a word in a document and highlights them.*

###ColorHighlighter
*Highlight a hex code in a document and the background highlight colour is changed to the colour.*
 

###More
[Useful post about configuring Sublime Text 2 and using snippets](http://www.nerdi.net/blog/2012/02/05/customize-your-sublime-text-2-configuration-for-awesome-coding/)

[List of useful plugins](http://net.tutsplus.com/tutorials/tools-and-tips/essential-sublime-text-2-plugins-and-extensions/)