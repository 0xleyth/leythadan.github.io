---
title:  "All about the top command"
mathjax: true
layout: post
comments: true
categories: media
---

The `top` command is a Unix utility that displays information about the running processes on a system, including their `CPU` and `memory` usage. When you run the `top` command, it displays a list of the processes that are currently running on the system, along with information about each process, such as its process ID (`PID`), `user`, `CPU usage`, and `memory usage`.

There are several fields that are displayed by the top command, including:

- PID: 
  - the process ID of the process
- USER: 
  - the user that owns the process
- PR: 
  - the priority of the process
- NI: 
  - the nice value of the process
- VIRT: 
  - the virtual memory usage of the process
- RES: 
  - the resident memory usage of the process
- SHR: 
  - the shared memory usage of the process
- S: 
  - the process state (e.g., S = sleeping, R = running)
- %CPU: 
  - the percentage of CPU usage by the process
- %MEM: 
  - the percentage of memory usage by the process
- TIME+: 
  - the total CPU time used by the process
- COMMAND: 
  - the command that was used to start the process

You can use various options and arguments with the `top` command to control the way it displays information and to customize its behavior. For example, you can use the `-o` option to sort the process list by a specific field, such as `CPU usage` or `memory usage`. You can also use the `-n` option to specify the number of iterations to display, or the `-d ` option to specify the delay between iterations.

{% if page.comments %}
<div id="disqus_thread"></div>
<script>
    /**
    *  RECOMMENDED CONFIGURATION VARIABLES: EDIT AND UNCOMMENT THE SECTION BELOW TO INSERT DYNAMIC VALUES FROM YOUR PLATFORM OR CMS.
    *  LEARN WHY DEFINING THESE VARIABLES IS IMPORTANT: https://disqus.com/admin/universalcode/#configuration-variables    */
    /*
    var disqus_config = function () {
    this.page.url = PAGE_URL;  // Replace PAGE_URL with your page's canonical URL variable
    this.page.identifier = PAGE_IDENTIFIER; // Replace PAGE_IDENTIFIER with your page's unique identifier variable
    };
    */
    (function() { // DON'T EDIT BELOW THIS LINE
    var d = document, s = d.createElement('script');
    s.src = 'https://EXAMPLE.disqus.com/embed.js';
    s.setAttribute('data-timestamp', +new Date());
    (d.head || d.body).appendChild(s);
    })();
</script>
<noscript>Please enable JavaScript to view the <a href="https://disqus.com/?ref_noscript">comments powered by Disqus.</a></noscript>
{% endif %}