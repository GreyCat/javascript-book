
# Label links 

Make all external links yellow by giving them class "external".
[html run nolinks]
<style>
.external { background-color: yellow }
</style>
<ul>
  <li><a href="http://google.com">http://google.com</a></li>
  <li><a href="/tutorial">/tutorial.html</a></li>
  <li>
   <a href="ftp://ftp.com/file.zip">ftp://ftp.com/file.zip</a>
  </li>
  <li><a href="http://nodejs.org">http://nodejs.org</a></li>
</ul>
[/html]

The result: 
[iframe src="tutorial/browser/dom/markLinks"]

=Hint 1

Find links using `getElementsByTagName`, filter them by `href.indexOf('://')`. 

Also check that the link may start with `http://javascript.info/...`. Such links are not external.

=Solution

The solution source: [play src="tutorial/browser/dom/markLinks"]

To skip links leading on current domain, `location.protocol` and `location.host` are used. They keep current scheme (http) and domain (javascript.info).

