Arke
====
Arke is a schedual optimizing mobile application.  
The concept: I have n amount of time to get from point X to point Y, find me the path that maxamizes the number of contacts/clients I can visit on the way.  
Ontop of this simple core concept, several additional features can easliy be implimented, such as:
* Adding static points to journy
* Automatic email of contacts 


The plan is to use a hybrid mobile application.  The web portion of the application will be a Ruby on Rails application running on Heroku, collection contact information using the Force.com API.  By using a remote hybrid application, it is simple to port across platforms, and updates to the application and underling algorithms is near instentanious. 
