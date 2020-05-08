it's **PE** <br>
I disassemble it with **IDA**: <br>
I checked **main** Function <br>
after some conditions it run at the end : <br>
``` ________(9, 22);``` <br>
so i checked this function and found it has some variables with static values then print it in praticular format : <br>
I run this function with c++ editor and found the flag 
```
#include <bits/stdc++.h>

using namespace std;

int main()

{
    int32_t a1 = 9 ;
    int32_t eax2;
    int32_t eax3;
    int32_t eax4;
    int32_t eax5;
    int32_t eax6;
    int32_t eax7;
    int32_t eax8;
    int32_t eax9;
    int32_t eax10;
    int32_t eax11;
    int32_t eax12;
    int32_t eax13;
    int32_t eax14;
    int32_t eax15;
    int32_t eax16;
    int32_t eax17;
    int32_t eax18;
    int32_t eax19;
    int32_t eax20;
    eax2 = a1 + 67;
    eax3 = a1 + 0x72;
    eax4 = a1 + 0x6c;
    eax5 = a1 + 0x69;
    eax6 = a1 + 59;
    eax7 = a1 + 59;
    eax8 = a1 + 0x74;
    eax9 = a1 + 0x65;
    eax10 = a1 + 40;
    eax11 = a1 + 94;
    eax12 = a1 + 39;
    eax13 = a1 + 0x6e;
    eax14 = a1 + 61;
    eax15 = a1 + 98;
    eax16 = a1 + 90;
    eax17 = a1 + 0x65;
    eax18 = a1 + 56;
    eax19 = a1 + 36;
    eax20 = a1 + 62;


    printf("%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c%c",static_cast<int32_t>(*reinterpret_cast<signed char*>(&eax14)),
 static_cast<int32_t>(*reinterpret_cast<signed char*>(&eax2)), static_cast<int32_t>(*reinterpret_cast<signed char*>(&eax18)),
 static_cast<int32_t>(*reinterpret_cast<signed char*>(&eax20)),
static_cast<int32_t>(*reinterpret_cast<signed char*>(&eax19)), static_cast<int32_t>(*reinterpret_cast<signed char*>(&eax3)),
static_cast<int32_t>(*reinterpret_cast<signed char*>(&eax6)), static_cast<int32_t>(*reinterpret_cast<signed char*>(&eax5)),
 static_cast<int32_t>(*reinterpret_cast<signed char*>(&eax12)), static_cast<int32_t>(*reinterpret_cast<signed char*>(&eax13)),
 static_cast<int32_t>(*reinterpret_cast<signed char*>(&eax17)), static_cast<int32_t>(*reinterpret_cast<signed char*>(&eax10)),
 static_cast<int32_t>(*reinterpret_cast<signed char*>(&eax9)),
 static_cast<int32_t>(*reinterpret_cast<signed char*>(&eax11)), static_cast<int32_t>(*reinterpret_cast<signed char*>(&eax7)),
static_cast<int32_t>(*reinterpret_cast<signed char*>(&eax4)), static_cast<int32_t>(*reinterpret_cast<signed char*>(&eax16)),
static_cast<int32_t>(*reinterpret_cast<signed char*>(&eax15)),
 static_cast<int32_t>(*reinterpret_cast<signed char*>(&eax8)));

}
```
```FLAG-{Dr0wn1ngDuck}```
