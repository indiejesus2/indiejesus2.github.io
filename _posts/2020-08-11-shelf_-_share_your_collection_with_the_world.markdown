---
layout: post
title:      "Shelf - Share Your Collection With The World"
date:       2020-08-11 15:26:20 +0000
permalink:  shelf_-_share_your_collection_with_the_world
---


I’m an avid book shopper, but not enough book shelves to display them all so many end up being boxed away for a future home. Whenever I go book shopping, I have trouble remembering whether I own a particular book or not. I would always curse myself for not keeping better track, until I vowed to create an app that could keep track of all the books I own.

When beginning the Sinatra project, it eventually dawned on me that this would be the perfect opportunity to use the project as a jumping off point to start my Shelf app. Unlike the popular Goodreads app that only keeps track of books read, Shelf is designed for instant access to a user’s library which can also keep track of pages read and books that have been read.

My initial thought was a user could have many books, but also a book could have many users, so I decided a join table that housed the user ids and book ids would be most efficient. This was pretty easy to set up, the challenge came when figuring out how to store a user’s individual progress in a book. For example, two separate users may have the same book on each of their shelves, but one might be only a few pages into the book while another user has completely finished it. Just as the project requires, and any website/app for that matter, a user should not be permitted to edit the data of another user.

Originally, I added columns to the book’s table, but quickly realized that encounters the same problem I just described above. So I had to remove the columns from books and add them to the joint table, users_books table, which is essentially a users library. This allowed a user to change the progress of a book without altering any other users progress in the same book.

The next challenge was displaying the user’s progress in a book, or a bookmark. I decided that a user could update the bookmark directly from the index page rather than having to navigate to an individual book page. Originally, the index page generates a users library by iterating and displaying books connected with that user, so I then tried to iterate through the user_books table to display pages read and completion of each connected book. It occurred to me that this wouldn’t suffice as I couldn’t administer another each method within an each method, each book was displaying multiple input forms  for pages read.

So I constructed the bookmark as an instance method that is called upon the current user that is also given the book id. So every book’s id that is iterated will be inputted into the bookmark method, which is then properly displayed with it’s corresponding book. It worked great, but doing all this directly from the index page made it somewhat difficult to see if the book details were updated or not.

That’s when I began looking into the gem Sinatra Flash, designed specifically for Sinatra so developers can display messages or alerts if there was some type of user error. Not only did it allow me to notify the user that a book’s information had been updated, it was a great tool to tell a user that a book needed specific information to be stored in their library, or when a new user attempts to sign up without the proper credentials or similar information as another user already registered.

This was a fun project to construct and I’m proud to have made it. The other great thing about this project is can be expanded for various collectors such as records, stamps, etc. In the future, I hope to further develop this project so users can search by genre or author, or display only books that have been completed. Hopefully one day we will all have a Shelf to admire, and will help people like me stop buying the same book three times.
