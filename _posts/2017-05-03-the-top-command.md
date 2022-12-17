---
title:  "All about the `top` command"
mathjax: true
layout: post
comments: true
categories: media
---
### What is it ?
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


### When is it useful ? 

The `top` command is a useful tool for monitoring the performance and resource usage of a Linux system. It can be used to view the running processes on the system, along with information about their `CPU` and memory usage, and to identify processes that are using a lot of resources.

There are several situations in which you might use the `top` command in Linux:

When you want to check the overall resource usage of your system, including `CPU` and memory usage, to determine if your system is running efficiently.
When you want to identify processes that are using a lot of resources, such as `CPU` or memory, so you can take action to optimize their performance or terminate them if necessary.
When you want to monitor the performance of a specific process, such as a server or a background task, to ensure that it is running smoothly and using resources efficiently.
When you want to troubleshoot performance issues on your system, such as slowdowns or high CPU or memory usage, by identifying the processes that are causing the issue.
When you want to monitor the performance of your system over time, by running the top command in batch mode (using the `-b` option) and redirecting the output to a file. This can help you identify trends and patterns in resource usage over time.


### To be used in conjunction with the top command 

Luckily, there are several other tools that can be used in conjunction with the `top` command to monitor and optimize the performance of a Linux system. Some of these tools include:

`ps`: 
- This command displays information about processes that are running on the system, including their process ID, user, CPU and memory usage, and command. It can be used to view the status of a specific process or to list all processes on the system.
free: This command displays information about the system's memory usage, including the total amount of memory available, the amount of memory used, and the amount of memory that is free.

`vmstat`: 
- This command displays information about the system's virtual memory and CPU usage, including the number of processes that are waiting to be run, the amount of memory that is used, and the amount of CPU time that is being used.

`iostat`: 
- This command displays information about the system's input/output (I/O) usage, including the amount of data that is being read and written to disk, and the average wait times for I/O operations.

`mpstat`: 
- This command displays information about the system's CPU usage, including the usage of individual CPUs or CPU cores, and the amount of time that is spent in different CPU states (e.g., user, system, idle).
These tools can be used together with the top command to provide a more complete picture of the performance and resource usage of a Linux system, and to help you identify and troubleshoot performance issues.





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