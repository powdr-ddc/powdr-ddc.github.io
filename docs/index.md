## Summary

Powdr is designed to be a social ski app to meet other riders around the world. Users will be able to create a user profile where they can upload pictures, state their skill level, list their home mountains, days logged, ect. Users will also be able to post to a shared community wall, allowing them to see posts only locally if they want based on GPS, or nationally if they want as well. 
They can meetup with other riders, share pictures, talk about ski/snowboard advice, or whatever they want to talk about. If they so please, users can add other riders and message them. Using the different GPS capabilites, the app will be able to check your distance traveled per ski day, and log your tracked distance into a leaderboard where you can compare with friends and other people internationally. 
To top it off, there will be a section in the app that will allow users to see the weather from various mountains of their choosing.

Intended Functionality:

Users will create a profile that they can customize to their liking. They can upload pictures, create a biography, see their personal stats such as days ridden or distance traveled, and choose from a list of their favorited mountains for easy access to the weather.
With a profile, the user can post to a shared community wall that is based off of GPS location, or a general international scope where users can see others from around their country. On this shared wall, users can comment on each others posts, upload pictures, and posts, to connect with 
other people around the world. If a user connects with someone on the app, they can send a friend request to the respective user and message them from within the app. If the social connection aspect is not alluring to some folks, they can instead choose to use the app for utility, allowing them to track the weather at different ski resorts, log their distance traveled for a certain day, 
and/or check the number of days they went skiing for a given season.

## Intended users

* People who want to meet others who enjoy skiing/snowboarding

	> As someone who goes skiing often, I want to meet other riders around me so I can make more friends who ski/snowboard and form a community in which we can improve together.
	
* People who lack friends that ski/snowboard

	> As someone who goes skiing way more often than any of my friends, I want to meet other solo riders so we can meetup at the mountain or carpool and hopefully befriend others who go skiing as frequently as me.

* People who are interested in the mountain weather

	> As someone who lives near multiple ski resorts and mountains, I want to check the weather of the various mountains to decide which one will have the best conditions for skiing so I can decide which mountain I should go to that day.

* People who are interested in logging their feet traveled per ski season

	> As someone with a competitive nature, I want to be able to log my stats on the app to track my feet traveled per season as well my total days ridden so I can compare it with my friends and others around the world, and hopefully climb to the top of the leaderboard!

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
		
	* GPS Feet Tracker Section
	
	  Screen for tracking distance traveled through GPS to upload to a leaderboard and share with friends/community.
    
* **Persistent data**

    * User Profile
	
	* Messages prior to connection loss
	
	* Community Wall prior to connection loss
	
	* Distance traveled for tracker
	
* **Device/external services**

	* [GPS](https://developer.android.com/training/location)
	
		* The system will use the service to ping the users location to find out weather and track them on the mountain. System should still be functioal without the service.
	
	* [Contacts](https://developer.android.com/reference/android/provider/ContactsContract)
	
		* Contacts will be pinged to find friends on the app. System is still functional without it.
	
	* [Camera](https://developer.android.com/guide/topics/media/camera)
	
		* Allows user to take picture from their camera to upload to their profile. System is functional without it.
	
	* Weather
	
		* [Open Weather API](https://rapidapi.com/community/api/open-weather-map)
		
		* [Weatherbit API](https://rapidapi.com/weatherbit/api/weather)
		
			* Obtains weather data to update the weather aspect of the app. System can still function without it.
		
   
## Server component

* **Functionality**

    * Weather Data
	
	  Holds the weather data for respective mountains
	
	* Friends List
	
	  Holds a database for a list of the user's friends
	
	* Messaging
	
	  Holds a database for user messages.
	
	* Community Wall Posts
	
	  Holds a database for main posts from community wall.
	  
* **Persistent data**

    * Messages
	
	* Community Wall
	
	* User Profile

	* Weather 
	
* **External services**

    * Weather
	
		* [Open Weather API](https://rapidapi.com/community/api/open-weather-map)
		
		* [Weatherbit API](https://rapidapi.com/weatherbit/api/weather)
		
			* Data base for weather data. App should still function without service.


## [Entity Relationship Diagram](powdr-erd.md)

## Stretch goals/possible enhancements 

* GPS distance tracking to track distance traveled throughout the season

* Tips and Tricks section for users to share with the community
	
* Event Page with listed snowboarding events like X Games
