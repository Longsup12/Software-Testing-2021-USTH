Ex 1.5:

a)
findLast:
The condition in the for loop is wrong. 
If we want to iterate through all the elements in the array then
the condition is i >= 0 (not >)
    
lastZero:
To find the last index of an element in an array,
we iterate through the array from the last element to the first element 
(not from the first element to the last element)    

countPositive:
The condition of if statement is wrong.
Positive elements are elements greater than 0 (not >=)  

oddOrPos:
The condition to determine whether a number is odd or not is that
the remainder divided by 2 must be non-zero (not equal to 1)

b)
Test cases that does not execute the fault:
findLast: x = [1, 0, 2], y = 0
lastZero: x = [1, 0, 2]
countPositive: x = [-1, 1, 2]
oddOrPos: x = [0, 1, 2]

c)
Test cases that execute the fault:
findLast: x = [0, 1, 2], y = 0
lastZero: x = [0, 1, 0, 2]
countPositive: x = [0, 1, 2]
oddOrPos: x = [-1, 0, 1]

f)
findLast:
    public int findLast(int[] x, int y) {
        for (int i = x.length - 1; i >= 0; i--) {
            if (x[i] == y) {
                return i;
            }
        }
        return -1;
    }
input: x = [0, 1, 2], y = 0
output: 0

lastZero:
    public static int lastZero(int[] x) {
        for (int i = x.length - 1; i >= 0; i--) {
            if (x[i] == 0) {
                return i;
            }
        }
        return -1;
    }
input: x = [0, 1, 0, 2]
output: 2

countPostitive:
    public int countPositive(int[] x) {
        int count = 0;
        for (int i = 0; i < x.length; i++) {
            if (x[i] > 0) {
                count++;
            }
        }
        return count;
    }
input: x = [0, 1, 2]
output: 2

oddOrPos:
    public int oddOrPos(int[] x) {
        int count = 0;
        for (int i = 0; i < x.length; i++) {
            if (x[i] > 0 || x[i] % 2 != 0) {
                count++;
            }
        }
        return count;
    }
input: x = [-1, 0, 1]
ouput: 2
