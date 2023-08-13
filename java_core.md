## Core

Order matters for the fields and blocks of code. You can’t refer to a variable before it has 
been defined:
```
{ System.out.println(name); } // DOES NOT COMPILE
private String name = "Fluffy";
```
```
public class Egg {
 public Egg() {
 number = 5;
 }
 public static void main(String[] args) {
 Egg egg = new Egg();
 System.out.println(egg.number);
 }
 private int number = 3;
 { number = 4; } }
```
Answer is 5. Fields and blocks are run first in order, setting number
to 3 and then 4. Then the constructor runs, setting number to 5
