two ways  
1:  
wget <link>    
wget <link>    
wget <link>    
$bvi level3.hash.bin  
copy "E1 6D 55 A5 5D 80 DD DD 52 A8 3E AB EA 57 2B 7B"  
type :q to leave  
$nano level3.py  
edit level_3_pw_check() into #level_3_pw_check() (in this way it won't ask for the pw  
add following codes:  
  (1)  
  target = bytes.fromhex("E1 6D 55 A5 5D 80 DD DD 52 A8 3E AB EA 57 2B 7B")  
  
  for pw in pos_pw_list:  
    if hash_pw(pw) == target:  
        print("Correct password:", pw)  
        print("Flag:", str_xor(flag_enc.decode(), pw))  
  or  
  (2)this one is better  
  for pw in pos_pw_list:  
    if hash_pw(pw) == correct_pw_hash:  
        print("Correct password:", pw)  
        print("Flag:", str_xor(flag_enc.decode(), pw))  
ctrl+x  
y  
enter  
$python level3.py  
there you get the flag :D  
  
2(not recommend):  
$nano level3.py  
see 7 passwords:  
"f09e", "4dcf", "87ab", "dba8", "752e", "3961", "f159"  
$python level3.py  
try those passwords one by one  
