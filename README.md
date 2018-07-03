# Core-java-technical-Question-interview

## String questions

1.     What is String in Java?
      
        *  A String represents a group of characters.
        *  Strings are constant in Java; their values cannot be changed after they are created.
      
2.     What are different ways to create Strings?

       *  There are two ways to create string objects in java. 
            * One is using new operator 
            * string literals. 
                 -> String s1 = new String("abc");
                 -> String s2 = "abc";

3.     What is String constant pool?
          
       * A String constant pool is a separate block of memory that JVM maintains for storing String objects.
         
          ->  String str = "abc"; // will be stored in String constant pool
          -> String str = new String("abc"); // will not be stored in St


4.     What is the difference between following statements :
         i) String str = “abc”;
         ii) String str = new String(“abc);
5.     How to compare two Strings in java program?
6.     What is the difference between comparing Strings with == operator and equals() method ?
7.     What is the difference between String, StringBuffer and StringBuilder classes ?
8.     What is String immutability and why is String immutable in Java ?
9.     How to Split String in java?
10.     What does String intern() method do?
11.     Are Strings thread-safe in Java?
12.     How to convert a String to int in Java ?
13.     How to convert String to LocalDate, LocalDateTime in Java ?
