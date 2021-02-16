---
layout: post
title:      "Notching A Birdie on the JS Course"
date:       2020-12-15 20:37:13 -0500
permalink:  notching_a_birdie_on_the_js_course
---


In the before times, I enjoyed going to the park with my friend to play Frisbee Golf. I'm not good, at all, but I'm too old to play ultimate frisbee so this is the next best thing. Continuing my theme of building projects that I would find useful, I thought an app that rated Frisbee Golf Courses would be fun to tackle.

Building the frontend and backend went smoothly, until I tried to establish a has-many relationship between FGC and comments. Because the backend is set up as an API using namespace formatting, the default method built into rails that sets up a foreign key connecting the two tables wouldn't work. Instead, after brushing up on Active Record Associations, I learned there was an option to specify the foreign key, which turned out to be successful.

The next problem to tackle was adding a comments section each DIV that held FGC info. Originally, text inputs were used to submit the comments to the backend, targeted using previousElementSiblings that stemmed from an "Add Comment" button. This looked clunky and certainly not dry. It was suggested that I build a comment form instead so that the data could be seamlessly passed to the backend.

It was the perfect solution to cleaning up my code while maintaining its functionality. Unfortunately, it also altered the display that was less than desirable. Comments were now rendering underneath the small comments form rather than above as it was originally intended. Could have left it as is, but instead I had to append the comments before I joined the comment form.

Right now, it's pretty basic looking app. But I have some ideas for it, like hovering over Frisbees to submit rating rather than a drop down menu. Filter capabilities such as by location or best ratings would also be a nice feature. Plus a fresh coat of paint wouldn't hurt either. Once this is all done, I can start working that, and then treat myself to a nice game of Frisbee Golf!

