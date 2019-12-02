
 
You can test aws s3 buckets without having to install aws cli , you need a valid authenticated `s3.console.aws.amazon.com` cookie.


Go to `https://signin.aws.amazon.com/signin` and log in 
Copy all your cookies and save it under `User\Credentials\Cookies\s3.console.aws.amazon.com.Cookie` in case you are using cazador.


To test aws buckets using http client like burp repeater we will need :

- Aws authenticated user  cookie 
- Aws csrf CSRF can be  grabbed by inspecting response from `https://s3.console.aws.amazon.com/s3/home`
or by using cazlib > 

```csharp
CazLib.V1.Robots.ThirdParty.Amazon.s3.Get_CSRF_Token(your_cookies_str);
```


To check bucket state , use the following request 

```http
POST /s3/proxy HTTP/1.1
Host: s3.console.aws.amazon.com
Content-Type: application/json;charset=utf-8
X-XSRF-TOKEN: XXXXXXXXXXXX
Content-Length: 188
Origin: https://s3.console.aws.amazon.com
Connection: close
Cookie: YYYYYYYYYYYYYYYYYYY
Cache-Control: max-age=0

{"region":"eu-central-1","headers":{"Content-Type":"application/x-amz-json-1.1","X-Amz-Date":"Sun, 01 Dec 2019 22:35:33 GMT"},"method":"GET","path":"ZZZZZZZZZ","operation":"HeadBucket"}
```


1. XXXXX is your csrf token
2. YYYY is  your cookie 
3. ZZZZZZZZZ is the bucket to test



You may observe the following 

If you sent expired cookies

>
 ![If you sent expired cookies](https://github.com/YasserGersy/cazador_unr/blob/master/imgs/invalid_cookies.png?raw=true " ")


If you sent invalid csrf token
>
 ![If you sent expired cookies](https://github.com/YasserGersy/cazador_unr/blob/master/imgs/invalid_cookies.png?raw=true "")


Bucket does not exist :
>
 ![If you sent expired cookies](https://github.com/YasserGersy/cazador_unr/blob/master/imgs/Bucket_not_existed.png?raw=true "")
 

Bucket Existed
>
 ![If you sent expired cookies](https://github.com/YasserGersy/cazador_unr/blob/master/imgs/bucket_existed.png?raw=true "")
 
Bucket is in another region
>
 ![If you sent expired cookies](https://github.com/YasserGersy/cazador_unr/blob/master/imgs/bucket_existed_in_another_region.png?raw=true "")
 
 
 Cazador has a plugin to test s3 buckets you can use it .
