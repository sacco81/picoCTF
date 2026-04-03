$wget <link>  
$nano level2.py.1   
find the pw  
decode chr(0x64) + chr(0x65) + chr(0x37) + chr(0x36)  
$python - <<'PY'  
> print(chr(0x64) + chr(0x65) + chr(0x37) + chr(0x36))  
> PY
pw:de76
$python level2.py.1
enter pw  


