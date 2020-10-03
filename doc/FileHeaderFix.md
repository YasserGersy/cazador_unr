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

%PDF-1.7"
25,50,44,46,2d,31,2e,37

OR

%PDF-1.5"
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



**Ref**
 - https://en.wikipedia.org/wiki/List_of_file_signatures
