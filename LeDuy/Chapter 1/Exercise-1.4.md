Ex 1.4:

a)
public static Vector union(Vector a, Vector b) {
        Vector vector = new Vector();
        vector.addAll(a);
        vector.addAll(b);
        return vector;
}

b) 
The use of raw type is valid in Java. However, it can mask bugs.
For example, when we want the vector returned from union() method containing
only elements of type String but when we add an object created from Student
class it is accepted. This may cause an error while the program is running

c)
This code will cause Exception:

	var a = new Vector();
        var b = new Vector();
        a.add("Duy");
        var student = new Student("Duy", 20);
        b.add(student);
        var c = union(a, b);
        for (int i = 0; i < c.size(); i++) {
            System.out.print((String) c.get(i));
        }

explain: 
ClassCastException: class Student cannot be cast to class String

d)
In order for the program not to encounter the above error, we should declare
the type of the elements that will be added to the vector.
For example: Integer, Float,... or other reference types.
If we want the union() method to be used for various data types, we need to
declare the generic method as follow:

public static <T> Vector<T> union(Vector<T> a, Vector<T> b) {
        Vector<T> vector = new Vector<>();
        vector.addAll(a);
        vector.addAll(b);
        return vector;
}
