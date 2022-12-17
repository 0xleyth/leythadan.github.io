---
title:  "Difference between DELETE and TRUNCATE IN MySQL"
mathjax: true
layout: post
comments: true
categories: media
---

In MySQL, the DELETE statement is used to delete rows from a table, while the TRUNCATE statement is used to delete all rows from a table and reset the auto-increment counter.

The DELETE statement allows you to specify a WHERE clause to filter the rows that should be deleted, while the TRUNCATE statement does not have a WHERE clause and will delete all rows from the table. For example:

```sql
    DELETE FROM users WHERE age < 18;

```

This DELETE statement will delete all rows from the users table where the age column is less than 18.

```sql
    TRUNCATE TABLE users;
```
This TRUNCATE statement will delete all rows from the users table and reset the auto-increment counter.

The DELETE statement is slower than the TRUNCATE statement because it has to delete each row individually and maintain the integrity of the database, while the TRUNCATE statement can simply reset the auto-increment counter and delete all rows in a single operation. However, the DELETE statement is more flexible because it allows you to specify a WHERE clause to filter the rows that should be deleted.

In general, it is best to use the TRUNCATE statement when you want to delete all rows from a table and reset the auto-increment counter, and the best use-case for the DELETE statement is to delete specific rows.

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