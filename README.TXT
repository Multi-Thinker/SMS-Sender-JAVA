========================
BUILD OUTPUT DESCRIPTION
========================

When you build an Java application project that has a main class, the IDE
automatically copies all of the JAR
files on the projects classpath to your projects dist/lib folder. The IDE
also adds each of the JAR files to the Class-Path element in the application
JAR files manifest file (MANIFEST.MF).

To run the project from the command line, go to the dist folder and
type the following:

java -jar "SMS_Sender.jar" 

To distribute this project, zip up the dist folder (including the lib folder)
and distribute the ZIP file.

Notes:

* If two JAR files on the project classpath have the same name, only the first
JAR file is copied to the lib folder.
* Only JAR files are copied to the lib folder.
If the classpath contains other types of files or folders, these files (folders)
are not copied.
* If a library on the projects classpath also has a Class-Path element
specified in the manifest,the content of the Class-Path element has to be on
the projects runtime path.
* To set a main class in a standard Java project, right-click the project node
in the Projects window and choose Properties. Then click Run and enter the
class name in the Main Class field. Alternatively, you can manually type the
class name in the manifest Main-Class element.
 How to Configure SMSLib:
There are 3 files available in Config Folder
1.      Comm.jar
2.      Win32com.dll
3.      javax.comm.properties
Step 1:- Copy comm.jar to
·         %JAVA_HOME%/lib  
[ In my case C:\Program Files\ Java\jdk1.7.0_03\lib ]
·         %JAVA_HOME%/jre/lib/ext
[ In my case C:\Program Files\ Java\jdk1.7.0_03\jre\lib\ext ]

Step 2:- Copy win32com.dll to
·         %JAVA_HOME%/bin
[In my case C:\Program Files\ Java\jdk1.7.0_03\bin ]
·         %JAVA_HOME%/jre/bin
            [ In my case C:\Program Files\ Java\jdk1.7.0_03\jre\bin ]
·         %windir%System32
             [ In my case C:\Windows\System32 ]

Step 3 : Copy javax.comm.properties to
·         %JAVA_HOME%/lib
            [ In my case C:\Program Files\ Java\jdk1.7.0_03\lib ]
·         %JAVA_HOME%/jre/lib
            [ In my case C:\Program Files\Java\jdk1.7.0_03\jre\lib ]
JAVA_HOME is path where jdk is installed
