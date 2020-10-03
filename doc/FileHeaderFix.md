# How to fix broken binary files


Hello in this tutorial , i am going to show you how to fix broken  which do not have magic bytes.

Suupose you have a pdf file , when you open it your , your pdf viewer can not parse it 

![Damaged pdf file](https://github.com/YasserGersy/cazador_unr/raw/master/imgs/damaged.pdf.file.PNG?raw=true)


if the reason is the missing magic bytes , the solution is simple , you just need to add the probber magic bytes.

if you searched , you would find that pdf header bytes are :  "%PDF-1.7" according to https://en.wikipedia.org/wiki/PDF


Converting   to the hexadecimal value :

```
%PDF-
25 50 44 46 2d

OR

%PDF-1.7
25,50,44,46,2d,31,2e,37

OR

%PDF-1.5
25,50,44,46,2d,31,2e,35


```
In linux you can use :

```
printf "25\x50\x44\x46\x2d\x31\x2e\x35" | cat - oldfile.pdf > newfile.pdf
```

In windows you can use cazador plugins 



![](https://github.com/YasserGersy/cazador_unr/raw/master/imgs/MagicFix.png?raw=true)

Opening the new file

![Works](https://github.com/YasserGersy/cazador_unr/raw/master/imgs/fixed.pdf.file.PNG?raw=true)


# Solving PentesterLab pdf_ssrf

You can say , the tool was inspired by https://pentesterlab.com/exercises/pdf_ssrf , the author used unix to solve the exercise and i had to use windows due to lake of machines.

Quoting 

```
 Introduction
A Server Side Request Forgery vulnerability allows an attacker to use the functionality of the web application to gain access to internal resources. In short, we are going to get the server to make HTTP requests (or over protocols) on our behalf.

This can be used to access internal pages, perform network scans, trigger behaviours in different systems...

In some cases, the application will use a headless browser (like phantomjs, wkhtmltopdf, weasyprint...) to generate a PDF. This challenge is based on the DefCon 2019 talk "Owning the clout through SSRF and PDF" by Ben Sadeghipour and Cody Brocious.

This challenge
In this challenge, the application uses Weasyprint to generate a PDF from a webpage. One very specific behaviour of weasyprint is that it will embed <link> tags as EmbeddedFile in the PDF. This will allow you to link to a file on the filesystem to get access to it.

In order to recover the content of the file, you will then need to inspect the content of the PDF to extract the EmbeddedFile section and decompress it using zlib. 
```

When you exploit the vulnerabilit and trigger the ssrf , the application will read your requested file , compress it and add to  the generated pdf.

For PDF embeded files , the data will be looks like :

```
embeddedFile blahblahblah STREAM gzip-Compressed-Data ENDSTREAM
```

We are interested in the data between `STREAM` and `ENDSTREAM` , you can use any hex editor to extract this data , and save it to a file.

  

![Extracting data](https://github.com/YasserGersy/cazador_unr/blob/master/imgs/Extracting-Compressed-data.png?raw=true)


The next step is to pre-append the Gzip magic Bytes  ` 0x1f, 0x8b, 0x08, 0x00, 0x00, 0x00, 0x00, 0x00`  to the file.


![Adding bytes](https://github.com/YasserGersy/cazador_unr/blob/master/imgs/Addgzipbytes.PNG?raw=true)

Now we can decompress the data using 
![Solved](https://github.com/YasserGersy/cazador_unr/blob/master/imgs/Solvedptlabssrfpdf.png?raw=true)



**Ref**
 - https://en.wikipedia.org/wiki/List_of_file_signatures
 - https://www.sweetscape.com/download/010editor/
 - https://pentesterlab.com/exercises/pdf_ssrf
 
 I hope you enjoyed.
 
