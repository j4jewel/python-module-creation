# python-module-creation
Creating a python module using the function https://github.com/j4jewel/password-check-function


Create a script named validator.py
vim  validator.py
---
Contents
```sh
def check(*,password=None,digit=3,alpha=3,special=2,length=8):
    
    if not password == None:
        
        alpha_count = 0
        digit_count = 0
        special_count = 0
        
        if len(password) >= length:
            
            for char in password:
                
                if char.isalpha():
                    
                    alpha_count += 1
                
                elif char.isdigit():
                    
                    digit_count += 1
                    
                else:
                    
                    special_count += 1
                    
            if alpha_count >= alpha and digit_count >= digit and special_count >= special:
                
                return True
            
            else:
                
                return False
        
        else:
            
            return False
        
    else:
        
        return False
```
Using the module 
---
----
```sh
import validator                       -- Importing the module, just like os,scapy
validator.check(password='abc123#$#')  -- using the module
True                                   -- result
```

