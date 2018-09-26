# Mobile Automation in real device using Appium

## TOOLS :
1. Ruby (I used v.2.5.1)
2. Cucumber, rspec, and bundler 
3. JAVA JDK
4. Android SDK
6. Appium
7. Appium Library
8. Text editor

## SOURCE :
1. Ruby for Windows (https://rubyinstaller.org/).
2. Appium (http://appium.io/)
3. Android SDK manager and ADB are bundling with android studio (https://developer.android.com/studio/)
4. Java JDK (http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)
5. Appium Library (https://rubygems.org/gems/appium_lib/versions/8.0.2)
6. Text editor (I used Atom: https://atom.io/)

## Installation Steps for Windows :

## Ruby Setup :
   1. Install Ruby
   2. Edit PATH variable and add new value "C:\Ruby25-x64\bin"
   3. Run Command Prompt
   4. Type gem install cucumber
   5. Type gem install bundler
   6. Type gem install rspec
   7. Type gem install appium_lib
  
## JAVA JDK and Android SDK Environment Variable:
   1. Install JAVA SDK
   2. Make a new variable with name: JAVA_HOME and value C:\Program Files\Java\java-8
   3. Make a new variable with name: ANDROID_HOME and value C:\Android\Android-sdk
   4. Edit PATH variable and add new value "C:\Program File\jdk x.x.x\bin"
      Note : the directory depend of your JDK and Android SDK directory. "x.x.x" is value of version you have installed.
   3. Check the JAVA already running by type "java -version" in command promt.

## Appium Setup:
   1. Download and run Appium installation in (https://github.com/appium/appium-desktop/releases/tag/1.7.0)
   2. Or you can Install Node.js first (https://nodejs.org/en/) and then open command prompt, type "npm install -g appium" then press enter.
   
## Run the Automation:
   1. Open atom text editor write the script and saved it
   2. Open Appium and start the server
   2. Open command prompt and go to saved script directory
   3. Type cucumber
          
## Capabilities Setup:
            platformName:'android',
            deviceName:'your device name',
            platformVersion:'your device version',
            udid:'Your unique device identifier of the connected physical device',
            appActivity:'.HomeActivity',
            appPackage:'Android app you want to run ex.com.example.android.myApp',
            newCommandTimeout:'How long (in seconds) Appium will wait for a new command'
            
 ### Getting udid by type in command promt:
     'adb devices'
            
 ### Getting appPackage :
   
   Type in command promt:

     'adb shell'
   Then open your apps for which you want to find the appPackage.
   Now run this command:
  
     dumpsys window windows | grep -E ‘mCurrentFocus’
   Then you can find the appPackage and appActivity
   
   
    
      
