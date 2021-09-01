**Introducing Cvescanner**

_Cvescanner is a plugin which allows you test target/s for unknown and known [exploits](https://cve.mitre.org/cve/search_cve_list.html)_

_The tools is working as [Nuclie Project](https://github.com/projectdiscovery/nuclei)  and of course  it uses [nuclei-Templates](https://github.com/projectdiscovery/nuclei-templates)_

**If you are using Cazador** open store and install Cvescanner 

![store](https://github.com/YasserGersy/cazador_unr/blob/master/imgs/Storebrowse_cvescanner.PNG?raw=true)

After enabling the plugin , click Plugins Menustrip and start Cvescanner , After plugin loads  Go to settings and Click update to get  the latest pushed exploits from nucleiTemplates.


![settings](https://github.com/YasserGersy/cazador_unr/blob/master/imgs/CvescannerDownloadedexploits.PNG?raw=true)

The application by default stores any downloaded repo under `App\Repos\` 

The tool will download the full repo latest commit ,  the needed-Exploits are located at `App\Repos\nuclei-templates-master\cves` 

**Now let's use the tool**
Cvescanner has 3 main sub-tools 
- An automator to test multiple targets and multiple exploits
- An explorer to debug your exploits , it only allows a single exploit and a single target per process , it is helpful in case you are debugging your exploits.
- the third is a generator which will help you to write your own exploits.


Take care the tools are in beta mode ,not all functions works properly.

Scanner :

To use the scanner , select your desired exploits , fill targets and click run.

![Scanner](https://github.com/YasserGersy/cazador_unr/blob/master/imgs/cvescanner1.PNG?raw=true)



To use the explorer  , select your desired exploit , define your target ,other  parameters are optional then  click run


![Explorer](https://github.com/YasserGersy/cazador_unr/blob/master/imgs/cvescanner2.PNG?raw=true)

To use generator : 
Play with it , you can refer to  
https://nuclei.projectdiscovery.io/templating-guide/  

Happy exploiting..
