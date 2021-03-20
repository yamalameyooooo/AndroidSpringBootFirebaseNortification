# AndroidSpringbootFirebase
This project sends notification to android devices from SpringBoot web api's including data

## Prerequisites
* Supported Android 4.1 or newer
* Android Studio 3.3.2 or higher
* google-services.json in app-level folder
* Spring Tool Suite or Spring supported IDE
* Firebase_Admin_SDK_key.json in src\main\resources\fcm folder

## Features
* Get token
* Send message with payload both **notification** and **data**
* Send message with **a token**
* Handle message both **foreground** and **background**
* Customize notification

## Steps for setup
* Check out the code
* Create a Google Cloud application at https://console.cloud.google.com/
* register that application in Firebase https://console.firebase.google.com/ by creating a new app (make sure to use the same pakage name as given in above preceeding step like com.shamsu.testApp)
* Go to Firebase console and click on project setting for the application you created.
* Under Project **settings>General>Your apps** and download the google-services.json and place the existing in the **app-level** folder for client.
* open **build.gradle** and put in **applicationId** attribute put "your_pakage_name" in value.
* Under Project **settings>Service Accounds>Firebase Admin SDK** click on "Generate new private key" and place it in **src\main\resources\fcm** folder for server.
* Open Andoid Studio and import the client code and use the SDK in project configurations which is present in your local system.
* You can either run in an emulator or build into a APK and install in a physical device
* Open Spring Tool Suite and import the server code as maven project.
* Change the name of Firebase_Admin_SDK_key.json in **application.properties** to the one which you pasted in **src\main\resources\fcm folder**
* Run the project as Springboot Application and hit the server rest POST API from postman with the sample RAW JSON data

## Sample Request data
* Use this sample request data to test the complete application and flow

> {<br>
>	"title":"Put the push notification title here",<br>
>	"message":"Put here push notification body here",<br>
>	"token":"Put the token from the mobile app which is running in the android/target device"<br>
> }

## For any further queries you can contact me at:
* :e-mail: Email shamsu602@gmail.com
* :video_game: Discord Server https://discord.gg/bWwMays



