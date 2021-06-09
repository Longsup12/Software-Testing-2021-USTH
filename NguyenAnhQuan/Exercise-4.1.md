```Java
import org.junit.Test;
import org.junit.runner.RunWith;
import org.junit.runners.Parameterized;
import org.junit.runners.Parameterized.Parameters;

import java.util.Arrays;
import java.util.Collection;
import static org.junit.Assert.assertTrue;

@RunWith (Parameterized.class)
public class subtest
{
    public int a, b, result;

    public subtest (int a, int b, int result)
    {
        this.a = a;
        this.b = b;
        this.result = result;
    }

    @Parameters
    public static Collection<Object[]> calcValues()
    {
        return Arrays.asList (new Object [][] {{3, 1, 2}, {5, 3, 2}});
    }

    @Test
    public void subtractionTest()
    {
        assertTrue ("Subtraction Test", result == Calc.sub (a,b));
    }
}
@RunWith (Parameterized.class)
public class multitest
{
    public int a, b, result;

    public multitest (int a, int b, int result)
    {
        this.a = a;
        this.b = b;
        this.result = result;
    }

    @Parameters
    public static Collection<Object[]> calcValues()
    {
        return Arrays.asList (new Object [][] {{2, 1, 2}, {2, 3, 6}});
    }

    @Test
    public void multiplicationTest()
    {
        assertTrue ("Multiplication Test", result == Calc.mul (a,b));
    }
}

@RunWith (Parameterized.class)
public class dividetest
{
    public int a, b, result;

    public dividetest (int a, int b, int result)
    {
        this.a = a;
        this.b = b;
        this.result = result;
    }

    @Parameters
    public static Collection<Object[]> calcValues()
    {
        return Arrays.asList (new Object [][] {{2, 1, 2}, {6, 3, 2}});
    }

    @Test
    public void divisionTest()
    {
        assertTrue ("Division Test", result == Calc.div (a,b));
    }
}
```