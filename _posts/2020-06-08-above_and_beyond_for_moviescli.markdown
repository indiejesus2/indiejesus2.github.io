---
layout: post
title:      "Above and Beyond for MoviesCLI"
date:       2020-06-08 01:18:31 -0400
permalink:  above_and_beyond_for_moviescli
---


For my project, I decided to select an Application Programming Interface (API) that involved movies. Since IMDb is an app that I use frequently, I thought it be fun to build my very own Command Line Interface (CLI) to explore movies with. Fortunately, there was an API available through a similar website, TMDB, that offered information for both films and television shows. It also featured a recommended and similar feature for exploring the data.

As I began to construct my program, I started to explore how the API was accessible and what was needed to extrapolate necessary information including GET requests. The requirements for this project included going one level deeper into the data scraped through the API; this is easier to perform with other APIs compared to the one available through API. 

I intended my CLI to allow a user to search for a movie title, and then retrieve basic information about the film such as the plot. TMDB offers an endpoint to search its database through a string, which reveals various information including release date, popularity and a brief synopsis of 20 films that closely relate to the keyword submitted. Well that was easy, only had to make one request to view the plot of a film. 

But what if the film I'm looking for isn't listed through the first page of results? The search is made by a keyword, so titles that aren't explicitly named may not return the film the user is seeking upon the first request, it may be in the second page of 20 films. So I decided to live dangerously and make numerous requests to gather all the results that yield from a keyword and sort them by popularity, a variable provided by TMDB.

Then I thought, there's more to a movie than its plot. I like to view the cast of a movie, who directed it or wrote it. That wasn't revealed through the first request of films. But it did include an id number that I can use to make a second request through the movie endpoint, that includes a plethora of parameters including credits. That's where I also discovered GET requests for similar movies and recommendations, a trending feature for viewers that need to know the next best thing to watch. That'd be fun to have in the program.

So even though the project didn't require making a second request, I decided to make one anyway to get the credits. First, I needed to configure a way to list the movies with an index to choose from the list of films rather than reveal random id numbers. I was able to enumerate the films stored in an arrary with an index, but in order to assign the number to that movie, each movie was instantiated with an index equal to 0. This made it possible to assign the index number created through the each method that corresponded to the film's place in the list.

In order to list similar movies and recommendations, I would have to make more requests as the endpoints provided by TMDB needed to be altered in order to fit my intentions. No problem, already done it twice before. After that I decided that my program had done enough scraping of data, and then I fixed the program to antipate user errors including entering a wrong id number or not following menu prompts.

I'm proud of my project. I'm looking forward to refactoring code and building it out more to take advantage of all the features the API has to offer. I felt that all the information and labs I have learned over the last couple weeks has really prepared me to tackle projects without hesitation.
