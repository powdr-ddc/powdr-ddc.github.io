## Team Members

* Adrian Anaya: Project leader, server side development, in charge of Ski Resorts and Weather

    * https://github.com/anayadrian1

* Jonah Rodriguez: In charge of the Wall and User screens, creation of most UI, server side development

    * https://github.com/JonahRodriguez281

* Austin West: Documentation of REST endpoints, build instructions, technology stack etc, server side development

    * https://github.com/mwest1997

## Summary

Powdr is a social media application designed for connecting skiers and snowboarders around the world. In a world where social interaction is becoming less and less frequent, we have taken it upon ourselves to hone our coding skills with a project that was not only important to us individually, but important to the ever-changing dynamic of interacting with others who share similar hobbies and passions. 

Our application allows New Mexicans to connect with each other through an intuitive and user-friendly UI . Users of the application will have several features available upon signing into the app. After signing in using their Google Sign-In credentials, users can create posts to share with others through a shared community wall by sharing photos and text posts. In addition to the wall, users can record data in relation to a ski trip, such as the distance traveled and total days ridden for a given season, as well as check the weather of various ski resorts in the New Mexico/Colorado area through the use of the World Weather Online Ski Weather API. If they desire, they can add other users to their friends list and message each other to plan future trips, meetups on the mountain, general talk, etc.  Powdr aims to connect skiers and snowboarders alike, to come together and experience all that the beautiful southwest wintersport community has to offer.

The key functional elements in the app as it stands allows a user to post to a community Wall, refresh the feed with a swipe refresh, check out a list of local ski resorts with their respective weather stats, and have a basic user profile with their biography, and a list of ski resorts and friends that can be filled if desired.

## [PDF Overview](pdf/powdr-overview.pdf)

## [State of Project](md/state-of-project.md)

## [Build Instructions](md/build-instructions.md)

## [Basic User Instructions](md/basic-instructions.md)

## Intended users

* People who want to meet others who enjoy skiing/snowboarding

	> As someone who goes skiing often, I want to meet other riders around me so that I can make more friends who ski/snowboard and carpool to the mountain, forming a community in which we can improve together.

* People who are interested in the mountain weather

	> As someone who lives near multiple ski resorts and mountains, I want to check the weather of the various mountains to decide which one will have the best conditions for skiing so that I can decide which mountain I should go to that day.

* People who are interested in logging their feet traveled per ski season

	> As someone with a competitive nature, I want to be able to log my stats on the app to track my feet traveled per season as well my total days ridden so that I can compare it with my friends and others around the world, and hopefully climb to the top of the leaderboard!

## Client component

* **Functionality**

	* Users will need to be logged in if they want to partake in any social aspects of the app such as the community wall or leaderboard for distance tracking. Parts of the app should be available to 
	users if they can't sign in, such as the weather portion of the app or the distance tracker without it recording the data.
	
	* The client will handle authentication with Google Sign In and pass the token to the server to verify with the provider.

	Users will be able to select from multiple screens:
	
	* User Profile
	
	  User profile screen with personal bio information and pictures for customization.
		
	* Community Wall
	
	  Shared wall among users to see each others posts based on gps, or nationally if they please.
		
	* Friends
	
	  A section for the friends list
		
	* Messaging
	
	  Screen for messaging
		
	* Weather
	
	  Screen for real-time weather data
		
	* GPS Distance Tracker
	
	  Screen for tracking distance traveled through GPS to upload to a leaderboard and share with friends/community.
    
* **Persistent data**

    * User Profile
	
	* Messages prior to connection loss
	
	* Distance traveled for tracker
	
* **Device/external services**
	
    * [Open Weather API](https://rapidapi.com/community/api/open-weather-map)
		
## Server component

* **Functionality**

    * Weather Data
	
	  Holds the weather data for respective mountains
	
	* Friends List
	
	  Holds a database for a list of the user's friends
	
	* Messaging
	
	  Holds a database for user messages.
	
	* Community Wall Posts
	
	  Holds a database for main posts from the community wall.
	  
* **Persistent data**

    * Messages
	
	* Community Wall
	
	* User Profile

	* Weather 
	
* **External services**
	
	* [Open Weather API](https://rapidapi.com/community/api/open-weather-map)
		
	* [Google Sign In](https://developers.google.com/identity/sign-in/web/sign-in)

## Server Side Design & Implementation

### [Wireframe](md/wireframe.md)

### [Entity Relationship Diagram](md/powdr-erd.md)

### [Data Model Implementation](md/entities.md)

### [Data Definition Language (DDL) SQL](ddl.md)

### [Technology Stacks](md/techstacks.md)

### [Endpoints](md/powdr-endpoints.md)

### [Repository Interfaces](md/interfaces.md)

### [OAuth2.0 Resource Server](https://github.com/powdr-ddc/powdr-service/blob/master/src/main/java/edu/cnm/deepdive/powdr/configuration/SecurityConfiguration.java)

### [REST Controllers and Application Logic Services](md/endpoints.md)

### [Javadocs Server](api/server/index.html)

### [Javadocs Client](api/client/index.html)

## Stretch goals/possible enhancements 

* GPS distance tracking to track distance traveled throughout the season

* Tips and Tricks section for users to share with the community
	
* Event Page with listed snowboarding events like X Games

### [Copyright & License info](md/copyright.md)
