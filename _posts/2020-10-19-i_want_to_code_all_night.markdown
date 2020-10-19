---
layout: post
title:      "I Want To Code All Night"
date:       2020-10-19 15:33:41 +0000
permalink:  i_want_to_code_all_night
---

Continuing my theme of building web applications that I wish I had in my life, I developed a Rails application that allows bands to keep track of their concerts. Bands will find it easy to log concerts by simply entering the date of the concert, price of admission and selecting a venue. If the venue does not exist in the database, a user can enter the information directly from the new concert web-page.

The site is ideal for bands and fans alike, as fans have access to their favorite local band’s shows, much like a concert flyer given out after concerts. Fans won’t have full access to adding new venues or concerts, but they can find look forward to upcoming shows nearby.

Fans that want to narrow down the concerts they want to view can search by date, band or venue. This is a useful feature, especially being able to handle multiple parameters. Of course this is doable, but the code became long with plenty of if statements. To clean up the code, I developed a class method that iterates over the parameters and stores them in a hash in a key/value relationship. So whether the concerts are being filtered by dates, or when a band plays at a particular venue, it can be handled by a single method.

I wanted the index to be able to handle multiple requests, including displaying all concerts that are logged into the database, a single band’s concerts or concerts that match the search parameters entered. This would mostly be an easy task at first, the real challenge was getting the view right. I wanted the web-page to alter depending on the request, whether it was single band that could display their name at the top, or a list of the concerts grouped by the artist. My initial thought was using the each method, but that would list the artists name multiple times along with each concert.

I came up with a couple solutions, but they were developed within the views and I was determined to correctly assign the controller the task of gathering the data. I eventually developed a solution that creates an empty hash to store concerts that either matched the search request or paired upcoming shows with their respective artists. It’s not as clean as I’d like but it accomplishes the task.

I began this product with a lot of ideas including linking multiple bands to a single concert or grouping bands by hometowns, but I logged plenty of hours and had to draw the finishing line somewhere. I look forward continuing to work on this project, as it offers countless features that can be developed and implemented. 
