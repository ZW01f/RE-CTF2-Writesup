so it's  **ELF64-bit**<br/>
we need the password to pass  <br/>
I used **ltrace** then  search for **strcmp(,)** function 
```
mohamed@DESKTOP-1TJHF7B:~$ sudo ltrace -o password ./alien_bin mans
Feed me the right password: mans
ERROR
mohamed@DESKTOP-1TJHF7B:~$ cat -n password |grep strcmp
     5  strcmp("mans", "bd23cf3f56baa86bc")                                       = 11 
```
 it compares my input with **"bd23cf3f56baa86bc"** so it's the password : <br/>
 ```mohamed@DESKTOP-1TJHF7B:~$ ./alien_bin
Feed me the right password: bd23cf3f56baa86bc
blip blop :) 
```
it's done ^_^

