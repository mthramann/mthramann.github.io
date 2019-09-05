---
layout: page
title: /projects
permalink: /projects/
---

# Projects

## [MBTA Map](https://mbta-thramann.herokuapp.com)
<br />This web app is an interactive map of the T (the Boston subway line) with upcoming train times and directions for each station. If the user allows location access from their browser, the app also plots the path to the nearest station, and displays distances to the 10 nearest stations in miles. The app also records which stations are clicked, and user locations. No other information is stored.

<br />This webapp uses the [Google Maps API](https://developers.google.com/maps/documentation/javascript/tutorial) and the [MBTA V3 API](https://www.mbta.com/developers/v3-api) to plot points on the map, and to get realtime train schedule data. The frontend is simple HTML and CSS, the server routes are written in JS with Node and Express, and the database is MongoDB, via MongoLab. The app is hosted on Heroku and linked to a [GitHub repo](https://github.com/mthramann/mbta).
          
<br />The initial iteration of this project was for the Web Development course at Tufts University, but the vast majority of the features are additions beyond the assignment. I also had to migrate the app from separate repos for frontend and server side to one repo, and then link that to the Heroku app, instead of manually deploying with the Heroku CLI as before.

## "Who Ate the Tuna Salad?" Google Action
<br />After going out to dinner one night, my girlfriend's mom (who works for a book publisher) quipped that there should be an app called "Who Ate the Tuna Salad?" to help parties itemize restaurant checks. As a joke, I wrote a Google Action so that when Google Assistant is prompted "Who Ate the Tuna Salad?", it will respond with a random quote from literature denying that the tuna salad was theirs. To my surprise, Google approved it, and the action has just over 24,000 monthly users.

<br />While making the action wasn't technically difficult, I had to practice many of the other skills that go into development. I had to read and interpret the Google Actions documentation, think about how a client (or girlfriend's mom) would interact with my idea, and consider how to deploy the action to be successful. This last facet was particularly new to me. I had to write a description and metadata for the action, research Google's preferences in approving actions, as well as write a privary policy.

## Password Counting
<br />Professor [Ming Chow](https://mchow01.github.io/) runs a password cracking competition for his security class. Students enter their cracked username:password combinations into a form. When the contest ends and the form is closed, Ming needs a program to count the number of accurate passwords each student cracked, and how many times each password was cracked. He posted the specifications for the format of his answers and entries, and challenged students to write such a program. This project is my fulfillment of his challenge.

<br />At first, I thought of writing the program in C, just so I could be absurdly efficient (a tempting priority). However, I ultimately used Python for a couple of reasons. Firstly, I knew Python would be a lot faster to develop. With C, this program might've taken me a day or two to write and debug, but with Python it only took me an hour. Secondly, I had to consider data structures. I wasn't too keen on writing yet another hash table, and I didn't want to bother with the dependency of the [GNU C Library](https://developer.gnome.org/glib/) if Ming wanted to compile elsewhere. Meanwhile, Python has ready-built associative arrays. Thirdly, writing this program in C would be very tedious. I'd have to efficiently allocate memory for handling unbounded size input lines, splice lines manually, implement or link data structures, clumsily deal with char* lengths, etc.. Many of these issues have effective idioms or solutions, but I wasn't interested in writing this program just to practice what I've done many many times before. Rather, I was glad to see how obvious sudocode easily translated into Python, and practice the language for white-board interviews.

<br />If Ming had thousands of students, I probably would've gone with C. At some point the time/memory savings are significant. However, Ming's class is usually less than one hundred students, so Python works just fine.

## Virtual Machine in C
<br />For this project, I implemented a virtual machine with eight registers and a 32 bit segmented memory in C. The program takes as input an executable file of 32 bit universal machine instructions (a 13 instruction set similar to assembly, with a few macros and AMD64 stack conventions) and runs the program. Because the machine had realistic performance standards, a large challenge of this project was to efficiently design abstractions and choose data structures. Furthermore, I had to account for implementing a 32 bit architecture on a 64 bit machine, where the virtual machine would run.

<br />As a follow-up to this project, I then profiled and refactored the virtual machine to run as efficiently as possible. This was an interesting process because I got to experience where implementation-specific bottlenecks lied, and see the trade-offs between clean abstractions and performance.

<br />This was a partner project with [Thomas Chan](https://github.com/thomaslchan) as part of the Comp40 course at Tufts University. Due to academic integrity, please contact me if you'd like to see the private repository.
