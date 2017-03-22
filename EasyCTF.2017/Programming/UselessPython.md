Challenge: Useless Python
----------------------------------------
Category: Programming
----------------------------------------
50 points 
----------------------------------------
Description:
```
Boredom took over, so I wrote this python file! I didn't want anyone to see it though because it doesn't actually run, so I used the coolest base-16 encoding to keep it secret. python 
```
<a href="./../files/42552c587e13c09d2873cf20c4a2a558f60a3a46_useless.py">useless.py</a>

The python scrypt is encoded with base16, decoder gives me this:
exec(chr(101)+chr(120)+chr(101)+.....)

Code:
```
with open ('base16.txt', 'r') as f:
    num = ''
    for char in f.read():
        m = char
        if m != '+' and m != '(' and m != ')' and m != 'c' and m != 'h' and m != 'r':
            num += m
        else:
            if num != '' and num != '+' and num != '(' and num != ')' and num != 'c' and num != 'h' and num != 'r':
                sim = chr(int(num))
                with open ('text.txt', 'a') as out:
                out.write(sim)
            num = ''
```
After a few iterations:
```
flag = 'easyctf{python_3x3c_exec_3xec_ex3c}'
priint flag
```

flag = 'easyctf{python_3x3c_exec_3xec_ex3c}'
