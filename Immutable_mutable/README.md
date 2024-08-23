# Inner working of python
![alt text](image.png)

- Byte code is not machine code
- cpython, jython, stackless, pypy  <-- implementations

# Immutable and mutable in python
- Defination
_Mutable: changable_
_Immutable: cannot change_

**Mutable data types are**: List, Set, Dictionary, Bytearray, Array

**Immutable data types are**: Integers, Floating-point numbers, Boolean, Strings, Tuples, Frozen set, Bytes

But, if I have a code like this:

```py
a = "hello"
print(a) #OUTPUT: hello
a = "world"
print(a) #OUTPUT: world
```
But, wasn't a string immutable? This question leads to a concept called **Garbage collection**.

Everything in python is an object. When we define the string "a", a reference to it is saved in the memory as shown:
![alt text](image-1.png)

Now, python detects that no one is now pointing at "hello", and hence deletes it's reference from the memory. This is called **Garbage Collection**.
So, it actually never changed, hence immutable :).
