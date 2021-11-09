# Java Sort Array
## Customize Sorting
### Example: Sort String[] based on length of each String
The following Java codes have three approaches:  
- implement the abstract method int compare(T o1, T o2) in Comparator<T> class
- using lambda
- still use Comparator<T> class's static factory method (pattern): comparingInt
```java
import java.util.Arrays;
import java.util.Comparator;

public class SortArrayCustomize {

    static public void main(String[] args){
        String[] strs = new String[]{"abbd", "ab", "abc", "afafaa", "d", "b"};
        Arrays.sort(strs, new Comparator<String>() {
            @Override
            public int compare(String o1, String o2) {
                return o1.length() - o2.length();
            }
        });
        for (String str : strs){System.out.print(str + " ");}
        System.out.println();

        strs = new String[]{"abbd", "ab", "abc", "afafaa", "d", "b"};
        Arrays.sort(strs, (a,b) -> a.length() - b.length());
        for (String str : strs){System.out.print(str + " ");}

        System.out.println();

        strs = new String[]{"abbd", "ab", "abc", "afafaa", "d", "b"};
        Arrays.sort(strs, Comparator.comparingInt(String::length));
        // Arrays.sort(strs, Comparator.comparing(String::length)); also works
        // Arrays.sort(strs, Comparator.comparingInt(s -> s.length())); also works
        for (String str : strs){System.out.print(str + " ");}
    }
}
```
#### comparingInt
>static <T> Comparator<T> comparingInt(ToIntFunction<? super T> keyExtractor)  
>Accepts a function that extracts an int sort key from a type T, and returns a Comparator<T> that compares by that sort key.  
>The returned comparator is serializable if the specified function is also serializable.  
>  
>Type Parameters:  
>T - the type of element to be compared  
>Parameters:  
>keyExtractor - the function used to extract the integer sort key  
>Returns:  
>a comparator that compares by an extracted key  
>Throws:  
>NullPointerException - if the argument is null  
>Since:  
>1.8  

#### [interface ToIntFunction<T>](https://docs.oracle.com/javase/8/docs/api/java/util/function/ToIntFunction.html)

This is a functional interface and can therefore be used as the assignment target for a lambda expression or method reference.
#### String::length

- The double colon (::) operator, also known as method reference operator in Java, is used to call a method by referring to it with the help of its class directly. They behave exactly as the lambda expressions. The only difference it has from lambda expressions is that this uses direct reference to the method by name instead of providing a delegate to the method.

### Related Leetcode Questions
- [1048. Longest String Chain](https://leetcode.com/problems/longest-string-chain/)


### References
- [Double colon (::) operator in Java](https://www.geeksforgeeks.org/double-colon-operator-in-java/)  
- [ToIntFunction](https://docs.oracle.com/javase/8/docs/api/java/util/function/ToIntFunction.html)  
- [Interface Comparator<T>](https://docs.oracle.com/javase/8/docs/api/java/util/Comparator.html#comparingInt-java.util.function.ToIntFunction-)
