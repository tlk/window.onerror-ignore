window.onerror-ignore
========================

Collection of javascript exceptions that are most likely created by badly written extensions, malware or other unknown sources. The errors were collected from website log-files using a window.onerror handler similar to https://github.com/tlk/window.onerror

I have filtered the errors, such that the [ignore.txt](ignore.txt) file only contains errors that I concluded could not be caused by the site itself. The (terrible) data format is: ```"<exception>" line: <number> col: <number> <js-source-url> <user-agent>```


#### How do you know it is safe to ignore?
I used this procedure: Let t1 and t2 be the start and end time of your log-files, then search all the javascript files that have been served from your site during that period. You can do `grep -r admwl .` in your (minified/compressed/uglify'ed) javascript directory to find any occurrences. It's easy when all versions of your (minified) js-files are stored in git or similar. If you find no occurrences of that string, then it should be safe to conclude that the error was triggered by something else than your code.

#### Why is this useful?
If you do not already keep a serverside log of javascript exceptions that take place in your web applications, I can only recommend you to start doing that. You will most likely discover a few new things about your applications, and as a side effect you will also discover that really weird things happens in the real world browser environments out there.

That is not surprising but it might clutter your log files. I have seen browsers that trigger several exceptions per page load due to what I assume is badly written extensions or malware, and it would be nice to be able to silence that stuff.

This ignore.txt can be used to filter your window.onerror logs. That is all.


#### See also

* https://github.com/tlk/window.onerror
* http://blog.errorception.com/2012/03/tale-of-unfindable-js-error.html
* https://gist.github.com/pamelafox/1878283
