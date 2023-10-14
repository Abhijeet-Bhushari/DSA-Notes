## Left Shift (<<)

1<<5 = 100000 = 32

To find whether a bit is set or not ina number then we just do logical & with the number which is formed when only that place is set. 

example: 
Check whether 7th bit is set or not in this number: 1 0 1 0 1 0 1 1 0 0

    1 0 1 0 1 0 1 1 0 0
    &
    0 0 0 1 0 0 0 0 0 0 
    -------------------
    0 0 0 0 0 0 0 0 0 0 <--- If result 0 then the bit is not set
    else if result is not 0 the bit is set

code: 
```
int a = 454;
int check = 7;
if( a & (1<<check) != 0) cout<<"The 7th bit is set"<<endl;
else cout<<"The 7th bit is not set"<<endl;
```