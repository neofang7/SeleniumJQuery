About
==================
Selenium is decent, but it's not great. It's a pain to deal with, and doesn't 
treat it's users like programmers. It just operates on a level that simply 
emulates real browsers. Which is nice.

Sometimes -- Usually, you want more. Most developers who have used jQuery know
how awesome it is at dealing with managing, examining, and manipulating dom 
structures, yet -- It's not always available, and no good api exists for using
it reliably within Selenium -- Until now. 

Install
==================
	$ git clone git@github.com:Nthalk/SeleniumJQuery.git # Checkout project
	$ cd SeleniumJQuery                                  # Step into dir
	$ ant test                                           # Build/test
	                                                     # Run example
	$ java -Dwebdriver.firefox.bin=/path/to/compatible/firefox-bin -jar dist/SeleniumJQuery.jar
	
Using as a Library
==================
After installing, you can reference it as an ivy library as it will be in your
ivy cache. It does not currently have a home on any maven/ivy repos.

For the current revision, your ivy.xml should have a dependency of:
	<dependency org="com.anteambulo" name="SeleniumJQuery" rev="0.1"/>
	
Or you could just build it and drop the dist dependency jars and the 
SeleniumJQuery jar in your classpath.

Requirements
==================
The only requirement is ant, as everything else should be pulled in by ant.

Example
==================
Please see: https://github.com/Nthalk/SeleniumJQuery/blob/master/example/com/anteambulo/SeleniumJQuery/example/Example.java
for a sweet example!

Development & Typical Usage
==================
Typically, you really need to see what is going on to develop a good scraper.
My setup is usually with Firefox 5.0, and I inject firebug, and some firebug properties into my drivers while I develop them. Afterwards, I use HtmlUnitDriver for production (and I silence it's excessively verbose output).
