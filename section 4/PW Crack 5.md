$wget  
$wget  
$wget  
$wget  
$nano level5.py  
```py
#level_5_pw_check()  
   with open("dictionary.txt") as f:  
        for line in f:  
            user_pw = line.strip()  '''
  
            user_pw_hash = hash_pw(user_pw)  
  
            if user_pw_hash == correct_pw_hash:  
                print("Found:", user_pw)  
                decryption = str_xor(flag_enc.decode(), user_pw)  
                print(decryption)
```

 $python level5.py
