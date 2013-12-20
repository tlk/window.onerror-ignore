window.onerror-blacklist
========================

Collection of javascript exceptions that are most likely created by badly written extensions, malware or other unknown sources.

The errors were collected using a window.onerror handler such as https://github.com/tlk/window.onerror

I haven't decided how to structure the findings, so for now the data format is: "<exception>" line: <number> col: <number> <js-source-url> <user-agent>

