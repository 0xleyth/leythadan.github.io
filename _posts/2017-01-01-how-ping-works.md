---
title:  "How the ping command works"
mathjax: true
layout: post
comments: true
categories: media
---

In Linux, the ping command is used to send an Internet Control Message Protocol (ICMP) "echo request" packet to a specified host to test the connectivity between the host and the device running the ping command. The host will respond to the echo request with an ICMP "echo reply" packet, which is used to measure the time it took for the packet to be transmitted and received.

When you run the ping command, it will continuously send echo request packets to the specified host at a rate of one packet per second, until you stop the command by pressing CTRL+C. For each packet that is sent, the ping command will display the round-trip time (RTT) it took for the packet to be transmitted and received, as well as other information such as the packet size and the packet loss rate.

The ping command works by sending an ICMP echo request packet to the specified host. The packet contains a header with the ICMP type and code, as well as a payload of data. The payload of an ICMP echo request packet is usually filled with data that is all zeros, but you can specify a different payload by using the -p option.

When the host receives the ICMP echo request packet, it will process the packet and send an ICMP echo reply packet back to the device that sent the request. The echo reply packet contains a header with the ICMP type and code, as well as a copy of the payload from the original echo request packet.

The ping command calculates the RTT by measuring the time it takes for the echo request packet to be transmitted and the echo reply packet to be received. It does this by using a timer in the operating system, which starts when the echo request packet is sent and stops when the echo reply packet is received. The RTT is then displayed by the ping command in milliseconds.

The ping command also calculates the packet loss rate by counting the number of echo request packets that are sent and the number of echo reply packets that are received. If the number of echo reply packets is less than the number of echo request packets, it means that some packets were lost during transmission. The packet loss rate is then displayed by the ping command as a percentage.

In addition to the standard options, the ping command also has several advanced options that allow you to customize the behavior of the command. For example, you can use the -i option to specify the interval between each packet, the -c option to specify the number of packets to send, and the -t option to specify the maximum number of hops that the packet should take before it is discarded. You can use the man ping command to see a full list of options and arguments for the ping command.


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