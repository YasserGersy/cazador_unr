# cazador-fileslooker
Look for juicy information in android apps


Here we are going to discuss and explain why the tool was created , and what it does.

 **Summary**


The tool is a one of cazador suite , with index 32 among other tools.

 **Purpose**
 
*FIles-Looker* is just a tool to read and search for specific paterns in order to extract useful information from apk files.

This discusses how to extract emails,urls,sub-domains and api keys from android apk file.


**Environment**

Windows OS 7 and higher.



**Tutorial from scratch**


*APK*
>
 Android PacKage (APK) is the package file format used by the Android operating system for distribution and installation of mobile apps and middleware.Extended from	JAR and ZIP formats.

- You can download any application apk file from google store using :
https://apkpure.com/


After downloading change extension to `.zip` 
if you tried to unzip/extract An apk file , you will find extracted files like : 



*Extracted files*

![ unzipped](https://github.com/YasserGersy/cazador_unr/blob/master/imgs/fm0.png?raw=true)


In this tutorial , we are going to use ApkTool instead for reverse engineering the pk file.

After downloading the ApkTool and the application Apk file , Run the tool with the following 

```
apktool_2.3.4.jar d fb.apk
```

Where fb.apk  is the target apk file  and it should be in the same directory where apktool lives otherwise add the full path.




*running the apktool*

![running the apktool](https://github.com/YasserGersy/cazador_unr/blob/master/imgs/fm1.png?raw=true)
A new directory will be created with the same apk file name , contains the generated files.


Run Cazador files looker , and specify the generated path.
Customize your search depending on what you want to collect.




*Finding email addresses*

![The tool looks for any email addresses](https://github.com/YasserGersy/cazador_unr/blob/master/imgs/fm2.png?raw=true)





*Finding urls with specific pattern*

![urls](https://github.com/YasserGersy/cazador_unr/blob/master/imgs/fm3.png?raw=true)






*You can make use of the other option Manipulator to extract  additional data , for example subdomains*

![subdomains](https://github.com/YasserGersy/cazador_unr/blob/master/imgs/fm4.png?raw=true)



[Check other tools](https://github.com/cazadorsuite)

