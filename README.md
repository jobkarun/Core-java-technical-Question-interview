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
         
          -> String str = "abc"; // will be stored in String constant pool
          -> String str = new String("abc"); // will not be stored in St


4.     What is the difference between following statements :
         i) String str = “abc”;
         ii) String str = new String(“abc);
         
         * A string literal is assigned to String variable str. Here, the JVM checks for a matching object in String constant pool. If              it is not available, it creates a new String object and stores in the pool. If the object is found, it simply creates a                  reference to it, but doesn’t create a new object.

         * JVM always creates a new object without refering the String constant pool.
         
         
5.     How to compare two Strings in java program?

          * Here are some ways to compare Strings in Java.

            1) == operator : Compares references of the obejcts, not the contents)
            2) equals() : Compares the contents of the Strings
            3) equalsIgnoreCase() : Compares two Strings irrespective of their case
            4) compareTo() & compareToIgnoreCase() : Compares two strings lexicographically
            5) contains() : check is a String contains specified sequence of characters

         * There are also methods like regionMatches(), startsWith() and endsWith() that are used for comapring Strings.


6.     What is the difference between comparing Strings with == operator and equals() method ?
7.     What is the difference between String, StringBuffer and StringBuilder classes ?
8.     What is String immutability and why is String immutable in Java ?

        ## String Constant Pool
            *Strings are created in a special memory area in java heap known as “String Intern pool”.
            *Java can have a string pool because strings are immutable.

            Note : Using String() constructor or any other String function like substring(), concat(), replace()
            etc which internally uses String() constructor always create new string constant in the pool unless we call the method intern().

       ## Security
           * String is widely used as parameter for many java classes, e.g. to obtain network connections,
             database connection urls, usernames/passwords etc. 
             If it were mutable, these parameters could be easily changed and could lead to security issues.
 
       ## Concurrency
          * Strings are implicitly thread safe because of immutability.
            Therefore, Strings can be shared across various different threads without the need of synchronization.

       ## Caching
          * Since Strings are immutable, they can be cached and perform better compared to mutable counterparts.
            This is the reason why Strings are preferred as keys in hashmaps.
       ## Class loading
          * String is used as arguments for class loading. If mutable, 
            it could result in wrong class being loaded (because mutable objects change their state).

 9.     What are different approaches to split a String in Java ?
         * Here are some approaches to split a String in Java.

           – Using String split() method
           – Using StringTokenizer

            * StringTokenizer is a legacy class retained for legacy reasons although its use is discouraged in new code.
 
10.     What does String intern() method do?

        * When the intern method is invoked, if the pool already contains a string equal to this String 

11.     Are Strings thread-safe in Java?
        * Since String objects are immutable, it is thread-safe and it can be shared between multiple 
          threads without external synchronization.

12.     How to convert a String to int in Java ?

         – Using parseInt()
         – Using valueOf()


13.     How to convert String to LocalDate, LocalDateTime in Java ?

           LocalDate newDate = LocalDate.parse("2016-08-23");
           System.out.println("Parsed date : " + newDate)

14.     Different String concatenation methods in Java

        *Java provides following ways to concatenate strings :

        1) Using + operator

        2) Using String concat() method

        3) Using StringBuffer/StringBuilder append() method

        4) Using String join() method (added in JDK 8)
