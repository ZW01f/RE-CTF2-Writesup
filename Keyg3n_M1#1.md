it's **ELF 64-bit** <br>
we need password to pass  <br>
I  disassemble with IDA and chek **Main** Function : <br>
```
eax5 = check_key(rdi4, rsi3);
    if (eax5) {
        rdi4 = reinterpret_cast<void*>("You made it, now keygen me!");
        printf("You made it, now keygen me!", rsi3);
    }
```
pass depends on **chek_key** so i checked it :  <br>
```
if (rax4 <= 7 || (rax5 = strlen(v2), rax5 > 10)) {
        printf("Nope <3");
        exit(0);
 ```
 ``` 
  if (v3 <= 0x3e7) {
        printf("Nope <3");
        exit(0);
```
it returns false (print"Nope") when **10>len(password)<=7**  and **sum of chars in password <= 999** :<br>
so it suppose to work if **7>len(password)<=10**0 and **password > 1000** <br>
i tried **zzzzzzzzzz** and it's worked : 
```
mohamed@DESKTOP-1TJHF7B:/home$ ./keygen.bin
Give me a pass
zzzzzzzzzz
You made it, now keygen me!mohamed@DESKTOP-1TJHF7B:/home$            
```
i tried another solution to show if I was right :  **aaabbbcccz**
```
mohamed@DESKTOP-1TJHF7B:/home$ ./keygen.bin
Give me a pass
aaabbbcccz
You made it, now keygen me!mohamed@DESKTOP-1TJHF7B:/home$
```
it's worked too ^_^


