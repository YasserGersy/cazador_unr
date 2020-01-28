
![alt tag](https://github.com/YasserGersy/cazador_unr/blob/master/imgs/cazador.png?raw=true)
[![Gitter](https://badges.gitter.im/cazadorapp/community.svg)](https://gitter.im/cazadorapp/community?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge)
[![GitHub issues](https://img.shields.io/github/issues/YasserGersy/cazador_unr.svg)](https://github.com/YasserGersy/cazador_unr/issues) 
[![Github Stars](https://img.shields.io/github/stars/YasserGersy/cazador_unr.svg?style=social&label=Stars)](https://github.com/YasserGersy/cazador_unr/) 
[![GitHub Followers](https://img.shields.io/github/followers/YasserGersy.svg?style=social&label=Follow)](https://github.com/YasserGersy/cazador_unr/)
[![Tweet](https://img.shields.io/twitter/url/http/YasserGersy.svg?style=social)](https://twitter.com/intent/tweet?original_referer=https%3A%2F%2Fdeveloper.twitter.com%2Fen%2Fdocs%2Ftwitter-for-websites%2Ftweet-button%2Foverview&ref_src=twsrc%5Etfw&text=Cazador%20-%20Automated%20Pentest%20Recon%20Scanner&tw_p=tweetbutton&url=https%3A%2F%2Fgithub.com%2FYasserGersy%2Fcazador_unr)
[![Follow on Twitter](https://img.shields.io/twitter/follow/YasserGersy.svg?style=social&label=Follow)](https://twitter.com/intent/follow?screen_name=YasserGersy)


**Cazador**

CazadorApp itself does not contain any tools , however the built plugins contain the following :


# Tools

*Listeners*
- HTTP Server
- DNS Server
- TCP Server
- POSTMessage Hooker
- Websocket Hooker

*Analyzers*
- HTTP
- JS-Files
- FileSystem
- Binary
- Packet

*Net Tools*
- Get DNS Records
- Resolve Hosts
- Reverse IPs
- Passive DNS
- DNS History 

*Text Tools*
- Text Processing 
- Block construct
- Format generator
- pattern creation
- Encrypt/Decrypt data
- Hash Identification
- Crackers
- Payload Generators
- Encoders/Decoders
- Poc Generators (Python , bash , HTML)

*Recon*
- Get Websites ScreenShots
- GET Subdomains (Scrabbing , Minning , DNS-brute-force,Http-brute-force)
 - Site categorizer 
- s3/GC bucket enumeration 
- Github Lister
- Ip History

 *Scanners*
- Detect Misconfiguration 
- Port/vulnerability/ssl scanner
- Vulnerability Exploiters
- Waf Detection

*Scrabbers*
- Download Android apps (APK)
- Travis-CI logs fetching

 
*Tools discussed separately* [here](https://github.com/YasserGersy/cazador_unr/tree/master/doc) 

 <a href="/imgs" >ScreenShots </a>



<!-- [Dig] <img src="https://github.com/YasserGersy/cazador_unr/raw/master/imgs/Dig0.png"/> -->
[scanner]<img src="https://github.com/YasserGersy/cazador_unr/blob/master/imgs/scanner0.png" />
[TcpListener]<img src="https://github.com/YasserGersy/cazador_unr/blob/master/imgs/tcplistener3.png"/>  
[FileMiner]<img src="https://github.com/YasserGersy/cazador_unr/raw/master/imgs/FIleMiner.png"/>  
[Subscrabber]<img src="https://raw.githubusercontent.com/YasserGersy/cazador_unr/master/imgs/Subscrabber.png" />
[Hpinger]<img src="https://github.com/YasserGersy/cazador_unr/blob/master/imgs/pinger0.png?raw=true" />



<a href="https://www.virustotal.com/gui/file/0a59af8b6c192e4a8c02eea5d11737defce08adae1fdf4abd5cc50a4554d7a3d/detection" >virustotal Scan result</a>


**if the app is not working proberly , Download the missing dlls, put them in application folder , beside the executable file**

**Some notes:** 

- This tool is meant primarily for bug hunnters (specially beginers).
- This tool is not backdoored with any malicious software/tracking .
- This tool contains bugs more than features so use it carefully.
- Connections are issued using  the .Net (SystemDotWeb) which is  slow and limited by design , consider using many threads, this will be replaced with another solution.
- Memory is not carefully managed so be carefull , do not use all the tools at the same time.
- Do not use it illegally 
- Tools starting with _ are not built yet , i added buttons to remmember writing them so i could build them in  future, hence no need to reverse engineer the tool in order to enable them , if you have time feel free to do it no problem.
- Many third-parties are used without permitssion no APIS used.
- The source code is not published because the tool is a beta and the code is uggly and worse than my hand writing.
- Project is planned to be open-source with the first release.
- Suggestions are deeply welcome. 
- Credits are reserved for all authors and third-parties.


**Linked IN**
- https://blog.intigriti.com/2019/07/02/bugbytes-25-to-scan-or-not-to-scan-gotcha-and-live-mentoring-by-zseano/
- https://pentester.land/newsletter/2019/07/02/the-5-hacking-newsletter-60.html
- https://securitytraning.com/bugbounty-with-cazador/
