it's ** Elf64 bit **  <br>
i run it and found it's a game <br>
I disassemble it with **IDA**  <br>
there's a **won** Function ,so I checked what'll 
happen will won the game <br>
a message with 'you win ' appears  and this function is called : 
```v3 = GetEncryptionKey();``` <br>
so this function : 
```
{
  unsigned int i; // [rsp+0h] [rbp-4h]

  if ( GetEncryptionKey(void)::isEncrypted )
  {
    for ( i = 0; i <= 0x17; ++i )
      GetEncryptionKey(void)::data[i] ^= 127 - (_BYTE)i;
    GetEncryptionKey(void)::isEncrypted = 0;
  }
  return GetEncryptionKey(void)::data;
}
```
so this function does  some operations on  **data**
and retruns it  
**data=[0x3c,0x2a,0x3e,0x28,0x3d,0x01,0x17,0x1d,0x01,0x13,0x07,0x2b,0x04,0x42,0x1f,0x2f,0x1b,0x06,0x04,0xf,0x34,0x50,0x41,0x15,0x00** 
so i run this python code to extrack data : 
```
>>> x=[0x3c,0x2a,0x3e,0x28,0x3d,0x01,0x17,0x1d,0x01,0x13,0x07,0x2b,0x04,0x42,0x1f,0x2f,0x1b,0x06,0x04,0xf,0x34,0x50,0x41,0x15,0x00]
>>> output = ""
>>> for i in range (0,24):
	x[i] =x[i]^(127-i)
	x[i] = chr(x[i])
	output += x[i]

	
>>> output
'CTCTF{never_w0n_thic_:(}' ``` <br>
flag : CTCTF{never_w0n_thic_:(} 