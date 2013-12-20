window.onerror-blacklist
========================

Collection of javascript exceptions that are most likely created by badly written extensions, malware or other unknown sources.

The errors were collected using a window.onerror handler such as https://github.com/tlk/window.onerror

It is my intention to restrict this blacklist to errors that are - assumingly - independent of the site(s) where they were found. As a consequence, errors that can be traced back to the local web application has been filtered out. When in doubt, I don't add it.

I haven't decided how to structure the findings, so for now the data format is: ```"<exception>" line: <number> col: <number> <js-source-url> <user-agent>```
