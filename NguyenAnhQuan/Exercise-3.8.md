```Java
import static org.junit.Assert.*;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.Collection;
import java.util.List;
import org.junit.After;
import org.junit.Before;
import org.junit.Test;
import org.junit.runner.RunWith;
import org.junit.runners.Parameterized;
import org.junit.runners.Parameterized.Parameters;

@RunWith (Parameterized.class)
public class DataDrivenMinTest {
    
        @Test
        public void testMinNumbers() {
                ArrayList<Integer> nums = new ArrayList<>();
                nums.add(90);
                nums.add(50);
                nums.add(30);
                nums.add(70);
                
                assertEquals(30, Min.min(nums));
        }
        @Test
        public void testMinStrings() {
                ArrayList<String> strs = new ArrayList<>();
                strs.add("D");
                strs.add("X");
                strs.add("A");
                strs.add("L");
                assertEquals("A", Min.min(strs));
        }
}
```