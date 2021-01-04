---
layout: post
title:      "Asynchronous JS and Promises"
date:       2021-01-04 04:21:50 +0000
permalink:  asynchronous_js_and_promises
---


As web applications become more advanced, the coding behind the screen will be loaded with multiple functions to display the webpage. Naturally, coding is completed in a linear fashion, or more specifically, from up to down, left to right. Some of these functions, particularly those gathering data, will take longer than other functions to complete. This can cause a variety of problems, such as slowing down the webpage from displaying or performing actions. If a function relies on another function that is still processing, an error could be thrown causing the application to malfunction or crash.
Asynchronous programming writes callbacks to complete their action in the background, allowing other functions to continue their actions. Some asynchronous callbacks include setInterval or setTimeout, used to perform actions after a designated time event has finished. More commonly, asynchronous is most valuable when a webpage has to retrieve data through a network request. The unknown amount of data that needs to be fetched can slow it from being displayed, making it necessary to queue other functions to execute in the meantime.
This is all done with the use of promises, signaling to the execution context that the function “makes a promise” to deliver some form of data or an error when it completes itself. Generally, the main thread of code will be executed while s are placed in an event queue to be executed after. This includes any actions or callbacks that rely on the promise to complete or fail its function.
A promise is a placeholder object for the completion or failure of the callback function. The data being retrieved, or Fetch, is the promise that will be delivered if coded correctly. Next, or “then”, the promise’s response will be resolved in the next callback function, most likely a JSON object to be rendered onto the webpage.  In the instances of failures, the promise has resulted in an error which can be “caught” and the error message can be reported to the user.
Any software engineer must fear a faulty webpage that doesn’t work properly or is too slow to load, causing a ripple effect of dissatisfied users and low page visits. When creating an advanced website that provides information along with other interactions such as live-streaming content or video chat conferences, it is imperative that programmers use asynchronous JS to allow their webpages to run smoothly. 

