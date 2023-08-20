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
 System.out.println(egg.number);//5
 }
 private int number = 3;
 { number = 4; } }
```
Fields and blocks are run first in order, setting number
to 3 and then 4. Then the constructor runs, setting number to 5
```
public void findAnswer(boolean check) {}
Take a look at the following method checkAnswer() in the same class:
public void checkAnswer() {
 boolean value;
 findAnswer(value); // DOES NOT COMPILE because it tries to use a variable that is not initialized
}
```
```
public void findAnswer(boolean check) {
        int answer;
        // int otherAnswer;
        int onlyOneBranch;
        if (check) {
            onlyOneBranch = 1;
            answer = 1;
        } else {
            answer = 2;
        }
        System.out.println(answer);
        System.out.println(onlyOneBranch); // DOES NOT COMPILE because it does not present in else section
```

Here are some tips to help you remember logical truth tables for &, |, and ^:
- AND is only true if both operands are true.
- Inclusive OR is only false if both operands are false.
- Exclusive OR is only true if the operands are different.
