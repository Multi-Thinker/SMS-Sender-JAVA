========================
#Instructions
========================

##How to Run:

After Configuring and placing the required libraries in folders as instruction there are two ways to use this application
###1. GUI:
Either run by command `java -jar "SMS_Sender.jar"` or double click on jar if your system is configured to run jar files it will run "GUI" version of application, You need to choose your port where you have attached SMS device/USB/GSM Modem, the right sidebar is where you will see history of your sent or sms in your database (if configured); double clicking the sidebar item will popup the sent sms body;
![ScreenShot](http://codeot.com/wp-content/uploads/2018/04/Screenshot-from-2018-04-04-10-44-33.png)
###2. CLI 
you can run `java -jar "SMS_Sender.jar port number message"` passing these three parameters it won't load GUI component and will trigger the component responsible for sending SMS and logging it to database(if configured); you can however not check history of sent sms in CLI. 

##How to Configure Sender:
1. You need to change SMS center in the Sender.java, you can leave it blank if your modem auto-configure or you might need to provide SMS center number there with country code
2. You can remove/comment the ODJBC (Database) functions if you don't need it, or you can provide TSN string;

###There are 3 files available in Config Folder
1.      Comm.jar
2.      Win32com.dll
3.      javax.comm.properties
####Step 1:- Copy comm.jar to
-         %JAVA_HOME%/lib  
[ In my case C:\Program Files\ Java\jdk1.7.0_03\lib ]
-         %JAVA_HOME%/jre/lib/ext
[ In my case C:\Program Files\ Java\jdk1.7.0_03\jre\lib\ext ]

####Step 2:- Copy win32com.dll to
-         %JAVA_HOME%/bin
[In my case C:\Program Files\ Java\jdk1.7.0_03\bin ]
-         %JAVA_HOME%/jre/bin
            [ In my case C:\Program Files\ Java\jdk1.7.0_03\jre\bin ]
-         %windir%System32
             [ In my case C:\Windows\System32 ]

####Step 3 : Copy javax.comm.properties to
-         %JAVA_HOME%/lib
            [ In my case C:\Program Files\ Java\jdk1.7.0_03\lib ]
-         %JAVA_HOME%/jre/lib
            [ In my case C:\Program Files\Java\jdk1.7.0_03\jre\lib ] JAVA_HOME is path where jdk is installed

Please feel free to improve it/[Contact me](mailto:talha@codeot.com). 
