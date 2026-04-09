$wget    
$wget  
$wget    
$bvi level4.hash.bin  
get following code:    
"64 C1 EF 00 36 A9 A8 D1 76 FB C3 81 C4 AB DA 52"       
nano level4.py  
edit level_4_pw_check() into #level_4_pw_check()  
add following code:  
```py  
target = bytes.fromhex("64 C1 EF 00 36 A9 A8 D1 76 FB C3 81 C4 AB DA 52")  
    
for pw in pos_pw_list:  
if hash_pw(pw) == target:    
print("Correct password:", pw)    
print("Flag:", str_xor(flag_enc.decode(), pw))    
  ```   
ctrl+x      
y       
level4edit.py    
y    
      
$python level4edi.py       
there u get the flag!       
