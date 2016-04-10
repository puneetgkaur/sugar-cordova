#Cordova Container for Sugar



# Instruction to setup the development environment

1. install npm

2. Git clone 3 repos : https://github.com/puneetgkaur/cordova-cli, https://github.com/puneetgkaur/cordova-lib, https://github.com/puneetgkaur/cordova-plugman into a directory

3. Run the following commands:

        cd cordova-plugman
    
        npm install
    
        sudo npm link
    
        cd ..
    
        cd cordova-lib
    
        npm install
    
        sudo npm link
    
        cd ..
    
        cd cordova-cli
    
        npm install
    
        sudo npm link
    
        npm link ../cordova-lib/cordova-lib cordova-lib
    
        npm link ../cordova-plugman/ plugman



# commands used to develop a sugar app using cordova

## creating a project

    cordova create "project directory" "project id" "project name"


## Add the sugar platform to your project

    cordova platform add sugar


## Building the project

### Normal build with no extra toolbox buttons

    cordova build sugar

### Adding extra toolbutton

If you have added extra toolbutton then compile your app using the following command :

    cordova build sugar -- noiframe

## Adding Plugins to your project

To add plugins to your project - copy the plugin you wish to add from the plugin folder of this repository, and paste in your project directory's plugin folder, follow the plugin documentation at the apache cordova's website or you can see the sample applications for sugar using that plugin in the sample apps directory of the plugin folder of this repo.

## Installing the xo in sugar

To install your xo in sugar environment :
  1. Find the .xo file in cordova project directory/platform/sugar/cordova folder

  2. Copy the file from the location and paste in sugar build

  3. Go to the sugar shell and issue the command - sugar-install-bundle <name of the cordova project>.xo

  4. You are through ! Run the sugar shell and open the activity ! - If you havent changed the icon, it shows cordova icon by default as activity icon.


Please make changes on sugar side to enable successful run of cordova plugins. This will cater to the backend of the API calls which are generated from the web app. Please look into - https://github.com/puneetgkaur/sugar-cordova/tree/master/changes%20in%20sugar%20build 
