# Exercise 9.2.3
## Answer questions (a) through (d) for the mutant on line 6 in the method <span style="font-family:Courier">sum()</span>.

```java
public static int sum(int[] x)
   {
      int s = 0;
      for (int i=0; i < x.length; i++)
      {
         s = s + x[i]; //mutant
      }
      return s;
   }
```
###(a) If possible, find test inputs that do not reach the mutant.
Can not find.

###(b) If possible, find test inputs that satisfy reachability but not infection for the mutant.
Can not find
(c) If possible, find test inputs that satisfy infection, but not propagation for the mutant.
x = [0, 0 ,0 ,0]
(d) If possible, find test inputs that strongly kill the mutants.
