Arke
====
Arke is a schedual optimizing mobile application.  
The concept: I have n amount of time to get from point X to point Y, find me the path that maxamizes the number of contacts/clients I can visit on the way.  

Ontop of this simple core concept, several additional features can easliy be implimented, such as:
* Adding static points to journy
* Providing phone-numbers for calling ahead
* Intigration with Google Calander
* Reoptimizing schedual if ahead or beind of expected time


Technologie
------------

The plan is to use a hybrid mobile application.  The web portion of the application will be a Ruby on Rails application running on Heroku, collection contact information using the Force.com API.

To make searching for contacts by location less complex, addresses will be converted to Lat/Long coordinets using the Google Places API and stored back to the users Salesforce account. 
