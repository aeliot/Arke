Arke
====
Arke is a schedule optimizing mobile application, developed by [Adam Eliot](http://adam.eliot.ca), [Jack Gettings](http://www.JGets.com), and [Bobby Chan](http://www.bobbychanblog.com) for the 2013 Dreamforce Hackathon.

This repository is mainly for documentation, with the individual components \(server, android, iOS\) housed in their own repositories.

Concept
---
I have n amount of time to get from point X to point Y, find me the path that maximizes the number of contacts/clients I can visit on the way.  

On top of this simple core concept, several additional features can easily be implemented, such as:
* Adding static points to journey
* Getting phone-numbers from Salesforce, for calling ahead
* Integration with Google Calendar, scheduling around appointments
* Re-optimizing schedule if ahead or behind of expected time


Technologies
------------
The plan is to use a hybrid mobile application. The web portion of the application will be a Ruby on Rails application running on [Heroku](http://www.heroku.com), collecting contact information using the Force.com API. Since the core logic of the application is run on Heroku, porting the application between different OS's is greatly simplified.

To make searching for contacts by location less complex, addresses will be converted to latitude & longitude coordinates using the [Google Places API](https://developers.google.com/places/) and stored back to the user's Salesforce account. Once latitude & longitude have been established, contacts can be isolated by their proximity to the users route in order to reducing the number of vertices that must be analyzed during optimization.

Challenges
-----------
The biggest challenge is being able to optimize the path through the graph in relatively good time. Doing the analysis using pure brute force is an extremely painful exercise that is unfathomably computationally expensive, so the trick will be to isolate sets of vertices and potential paths that are more likely to produce a good result. The trade off here is that the result presented to the user will not be the mathematically optimal path, but will instead be a balance between path optimization and algorithm optimization, because there is no use in generating the optimal path if the user has already given up waiting.
