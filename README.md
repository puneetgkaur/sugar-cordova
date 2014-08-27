#Cordova Container for Sugar

## Updating Sugar to contain cordova container

1. Add the folder named cordova from "changes in sugar build" folder to the jarabe folder in sugar

2. There is a little change in apisocket.py , need to add a function named cordova in the Activity Class and import the CordovaSocket.py file from jarabe.cordova

## Setup the environment for sugar cordova

1. Install Node.js and npm
2. git clone this repository in a directory
3. cd to cordova-cli folder of this repository and issue the command npm link inside the folder
4. To create a new project : issue the command - cordova create <name of the project directory> <project id> <project name> 
5. To add the sugar platform to your project :
   1. Copy the 'sugar' directory from this repo into :
	    a) Linux or mac users : in ~/.cordova/lib
            b) Windows - C:\<User name>\.cordova 

   2. Issue the command : cordova platform add sugar inside the project directory created above

6. Build your web app - make changes in www or copy your cross platform cordova app in www folder of the project directory you created in step 3

7. Make Native Sugar application from your web app :
                    
   1. If you dont have much knowledge of sugar and just wish to port your web application to the sugar environment then make your .xo by giving the command : cordova build sugar ( no arguments) inside your cordova project directory

   2. If you know about the sugar environment and would like to make use of sugar web to make your activity then build the project with the command : cordova build sugar --noiframe inside your cordova project directory

   3. A note to windows user :  install 7zip and set the environment variable ZIPCOMMAND with the command
set ZIPCOMMAND="c:\Program Files\7-Zip\7z.exe" a -r -tzip -aoa before giving the build command

## Adding Plugins to your project

To add plugins to your project - copy the plugin you wish to add from the plugin folder of this repository, and paste in your project directory's plugin folder, follow the plugin documentation at the apache cordova's website or you can see the sample applications for sugar using that plugin in the sample apps directory of the plugin folder of this repo.

## Installing the xo in sugar

To install your xo in sugar environment :
  1. Find the .xo file in cordova project directory/platform/sugar/cordova folder

  2. Copy the file from the location and paste in sugar build

  3. Go to the sugar shell and issue the command - sugar-install-bundle <name of the cordova project>.xo

  4. You are through ! Run the sugar shell and open the activity ! - If you havent changed the icon , it would probably be that of cordova - so watch out :-)
