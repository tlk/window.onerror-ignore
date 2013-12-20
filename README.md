window.onerror-blacklist
========================

Collection of javascript exceptions that are most likely created by badly written extensions, malware or other unknown sources.

The errors were collected using a window.onerror handler such as https://github.com/tlk/window.onerror

It is my intention to restrict this blacklist to errors that are independent of the site(s) where they were found. As a consequence, web application specific errors are excluded. When in doubt, I don't add it.

I haven't decided how to structure the findings, so for now the data format is: ```"<exception>" line: <number> col: <number> <js-source-url> <user-agent>```


#### Why is this useful
If you do not already keep a serverside log of javascript exceptions that take place in your web applications, I can only recommend you to start doing that. You will most likely discover a few new things about your applications, and as a side effect you will also discover that really weird things happens in the real world browser environments out there.

That is not surprising. It might clutter your log files though. I have seen browsers that trigger several exceptions per page load due to what I assume is badly written extensions or malware, and it would be nice to be able to silence that stuff.

This blacklist can be used to filter your window.onerror logs. That is all.
