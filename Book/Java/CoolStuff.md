# String
The JVM checks the String Constant Pool. If the string does not exist then a new string instance is created and placed in the pool if the string exists then it will not create a new object rather it will return the reference to the same instance. The cache which stores these string instances is known as String Constant pool or String Pool. In earlier versions of Java up to JDK 6 String pool was located inside **PermGen**(Permanent Generation) space. But in JDK 7 it is moved to the main heap area.

# Tại sao boolean value chỉ cần 1 bit giá trị để lưu true/false (1/0) mà cần tận tới 1byte?
https://docs.oracle.com/javase/specs/jls/se8/html/jls-17.html#jls-17.6

<!--stackedit_data:
eyJoaXN0b3J5IjpbMjQ5MzI3MDM2LDEwNDczODYyMzUsMTIzMz
E3MjgyOF19
-->