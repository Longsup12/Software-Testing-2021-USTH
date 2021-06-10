# Ex 1.4: The following exercise is intended to encourage you to think of testing in a more rigorous way than you may be used to. The exercisealso hints at the strong relationship between specification clarity, faults, and test cases

### a) Write a Java method with the signature

```java
public static Vector union (Vector a, Vector b)
```

### The method should return a Vector of objects that are in either of the two argument Vector

``` java
import java.util.Vector;

class Vector { 
	public static Vector union(Vector a, Vector b) { 
		Vector c = new Vector(); 
		c.addAll(a); 
		c.addAll(b); 
		return c; 
	} 
	public static void main(String[] arg) { 
		Vector a = new Vector(); 
		a.add(9); 
		Vector b = new Vector(); 
		b.add(5); 
		Vector c = union(a, b); 
	} 
} 
```

### b) Upon reflection, you may discover a variety of defects and ambiguities in the given assignment. In other words, ample opportunities for faults exist. Describe as many possible faults as you can. (Note: Vector is a Java Collection class. If you are using another language, interpret Vector as a list.)

* There has no verification statement to check whether two vectors are empty

### c) Create a set of test cases that you think would have a reasonable chance of revealing the faults you identified above. Document a rationale for each test in your test set. If possible, characterize all of your rationales in some concise summary. Run your tests against your implementation.

Test case [1]  
Vector a = new Vector()  
Vector b = new Vector()  

Test case [2]  
Vector a = new Vector();  
a.add(9)  
Vector b = new Vector();  

Test case [3]  
Vector a = new Vector();  
Vector b = new Vector();  
b.add(5)  

### d) Rewrite the method signature to be precise enough to clarify the defects and ambiguities identified earlier. You might wish to illustrate your specification with examples drawn from your test cases.
```java
public static Vector union(Vector a, Vector b, boolean inv = False)
{
  if (a.isEmpty() && b.isEmpty()) return Null;
  else
  {
    if (inv)
    {
      Vector c = new Vector();
      c.addAll(b);
      c.addAll(a);
      return c;
    }
    else
    {
      Vector c = new Vector();
      c.addAll(a);
      c.addAll(b);
      return c;
    }
  }
}
```
