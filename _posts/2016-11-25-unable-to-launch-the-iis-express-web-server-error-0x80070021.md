---
layout: post
title: Unable to launch the IIS Express Web Server - Error 0x80070020
---

I recently got an error 0x80070020 when trying to launch IIS Express.

```
Unable to launch the IIS Express Web server.

Failed to register URL "http://localhost:5849/" for site
application "/". Error description: The process cannot access the file
because it is being used by another process. (0x80070020)
```

In order to find out which process is unsing the port I used netstat.

```
P:\>netstat -ano | findstr 58499
  TCP    127.0.0.1:53500        127.0.0.1:58499        SYN_SENT        8156
  TCP    [::1]:53499            [::1]:58499            SYN_SENT        8156
  TCP    [::1]:58499            [::1]:58499            ESTABLISHED     8156
```

With that information it's a simple task to kill the process in task manager and all is well again.