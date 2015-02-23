window.onerror-blacklist
========================

Collection of javascript exceptions that are most likely created by badly written extensions, malware or other unknown sources. The errors were collected using a window.onerror handler such as https://github.com/tlk/window.onerror

The [blacklist.txt](blacklist.txt) file only contains errors that I concluded could not be caused by the site itself, and the data format is: ```"<exception>" line: <number> col: <number> <js-source-url> <user-agent>```


#### How do you know that it's safe to include in the blacklist and to ignore?
I used this procedure: Let t1 and t2 be the start and end time of your log-files, then search all the javascript files that have been served from your site during that period. You can do `grep -r admwl .` in your (minified/compressed/uglify'ed) javascript directory to find any occurrences. It's easy when all versions of your (minified) js-files are stored in git or similar. If you find no occurrences of that string, then it should be safe to conclude that the error was triggered by something else than your code.

#### Why is this useful
If you do not already keep a serverside log of javascript exceptions that take place in your web applications, I can only recommend you to start doing that. You will most likely discover a few new things about your applications, and as a side effect you will also discover that really weird things happens in the real world browser environments out there.

That is not surprising. It might clutter your log files though. I have seen browsers that trigger several exceptions per page load due to what I assume is badly written extensions or malware, and it would be nice to be able to silence that stuff.

This blacklist can be used to filter your window.onerror logs. That is all.


#### See also

* http://blog.errorception.com/2012/03/tale-of-unfindable-js-error.html
* https://gist.github.com/pamelafox/1878283
