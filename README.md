Arke
====
Arke is a schedule optimizing mobile application.  
The concept: I have n amount of time to get from point X to point Y, find me the path that maximizes the number of contacts/clients I can visit on the way.  

On top of this simple core concept, several additional features can easily be implemented, such as:
* Adding static points to journey
* Providing phone-numbers for calling ahead
* Integration with Google Calender, scheduling around your appointments
* Re-optimizing schedule if ahead or behind of expected time


Technologies
------------

The plan is to use a hybrid mobile application.  The web portion of the application will be a Ruby on Rails application running on Heroku, collecting contact information using the Force.com API.

To make searching for contacts by location less complex, addresses will be converted to latitude & longitude coordinates using the Google Places API and stored back to the user's Salesforce account. 
