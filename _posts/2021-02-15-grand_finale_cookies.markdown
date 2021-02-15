---
layout: post
title:      "Grand Finale: Cookies!"
date:       2021-02-15 21:52:20 +0000
permalink:  grand_finale_cookies
---


One of the first roadblocks I encountered was handling the data after making a fetch request for users. Users have many records that include the date of the record and how many calories were imputed for the day. Then each record has an associated day of items and each item’s calories. 

The returned data was deeply nested, which means parsing the data would be long and potentially convoluted. I thought the best approach would be to make two separate requests, one for the users and the associated records, and a second request of the records and the associated days. The second fetch request is made when the link to the user’s records is clicked.

The chosen method allowed the app to work to an extent, until a new record or item was submitted to the API. While the components state was being updated with the new data, the props passed through to other components wouldn’t register. 

The workaround was using componentDidUpdate, which would keep track if the prevProps were the same as the current props. Specifically, the records array length of the prevProps would be compared to the current props, and if they did not match, another fetch request would be made for a user’s records.

I originally intended for the project to use an external API that already had a database filled with various food items and registered calories. I envisioned that similar to other calorie counting apps, a user could find an item through the search and not have to know the calories by heart. That will be the next major breakthrough I can tackle for this app.

Truthfully, the app is not fully functional considering there isn’t a way for users to login and have sole control over their records. Setting up a password and authentication will be the next priority.

