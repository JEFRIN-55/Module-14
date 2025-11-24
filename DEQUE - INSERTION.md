# Exp.No:39  
## DEQUE - INSERTION

---

### AIM  
To write a Python program to insert elements at REAR END of deque using a collection built-in function.

---

### ALGORITHM  

1. Import the `deque` class from the `collections` module.  
2. Initialize an empty deque.  
3. Start an infinite loop using `while True`.  
4. In each iteration, take input from the user.  
5. If the input is an empty string, break the loop.  
6. If the input is not empty, convert it to an integer and append it to the deque.  
7. After the loop ends, append the values `14` and `15` to the deque.  
8. Print the message `"The deque after appending at right is :"`.  
9. Print the contents of the deque.  

---

### PROGRAM  

```python
# Reg.No- 212223060104
# Name- JEFRIN INOLA J 

import collections
n1 = input("Enter first value: ")
n2 = input("Enter second value: ")
n3 = input("Enter third value: ")

de = collections.deque([n1, n2, n3])

de.append('h')
de.append('o')
de.append('n')

print("The deque after appending at right is:")
print(de)
```
---
### OUTPUT
![image](https://github.com/user-attachments/assets/5ff39b13-13f3-4458-b6f6-742a588eb258)

---
### RESULT
Thus, the Python program to insert elements at REAR END of deque using a collection built-in function was successfully implemented and verified.
