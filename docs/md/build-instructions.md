## Build Instructions

### Cloning the project

 First, you will want to clone service project. 
Repository can be found here: [Powdr Service](https://github.com/powdr-ddc/powdr-service)

1. To clone the project navigate to the green "Code" button at the top of the page.

2. Ensure that the SSH option has been selected then copy the link provided.

3. Open in IntelliJ and select "Get from Version Control".

4. Paste the link you copied from step 3 and click "clone".

 Next, you will want to clone the Android project.
Repository can be found here: [Powdr Android](https://github.com/powdr-ddc/powdr)

1. To clone the project navigate to the green "Code" button at the top of the page.
   
2. Ensure that the SSH option has been selected then copy the link provided.
   
3. Open in IntelliJ and select "Get from Version Control".
   
4. Paste the link you copied from step 3 and click "clone".

### Running the project

**NOTE:**
An API Key is required for this project to compile. A powdr.properties file will be sent personally with the API information as well as the other fields required for the project to build. Download the powdr.properties file into the service directory of your project folder.

First, you will need to open the service project. 

1.To run the server, you will have to navigate to the PreloadLauncher class, and run the program 
until IntelliJ tells you that the program has started.

2. Next, you will have to navigate to the ServiceLauncher, and run that program and have it running in 
the background while using the android app.

Second, open the android project and click the green "Run" button. Both the server and app should 
be running, building, and ready to go at this point.
 