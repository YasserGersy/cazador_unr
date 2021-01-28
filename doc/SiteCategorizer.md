Hi


 This tool allows you to automate sites categorization  using multiple APIS.

- ![Damaged pdf file](https://github.com/YasserGersy/cazador_unr/raw/master/imgs/SiteCat3.png?raw=true)

**Video**

https://vimeo.com/504801478

Site categorizers uses the following providers :

-  Fortiguard
-  Brandfetch
-  whoisxmlapi
-  klazify
-  WebShrinker

Urls:

- https://www.fortiguard.com/webfilter?q=
- https://api.brandfetch.io/v1/industry
- https://website-categorization.whoisxmlapi.com/api/v1?apiKey=$KEY$&domainName=$DOMAIN$
- https://www.klazify.com/api/categorize
- https://api.webshrinker.com/categories/v3/

All requires api key except `Fortiguard` .it allows unauthenticated calls no api-key required.

**ScreenShots**

The plugin interface :

- ![Damaged pdf file](https://github.com/YasserGersy/cazador_unr/raw/master/imgs/SiteCat0.png?raw=true)

When testing Alexa top 50 , here is the result :

- ![Damaged pdf file](https://github.com/YasserGersy/cazador_unr/raw/master/imgs/SiteCat1.png?raw=true)

If a provider requires Api token and the token is not found , the plugin will highlight the missing ones:

- ![Damaged pdf file](https://github.com/YasserGersy/cazador_unr/raw/master/imgs/SiteCat2.png?raw=true)

You can provide api token by following :

 - ![Damaged pdf file](https://github.com/YasserGersy/cazador_unr/raw/master/imgs/SiteCat5.png?raw=true)

**Default Behaviur**:

 The tool considers the performance , best result , unnecessary traffic , the tool allows users to use multiple providers , the current configurations instruct the tool to fetch cached values first , if not found it will use any enabled available provider to get the requested site's category.
 
The caching process can not be turned off ,the application caches all values to avoid multiple requests , however you can specify if you want a cached category or a fresh one.

Good Luck
