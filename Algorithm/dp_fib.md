# Dynamic Programming

Three steps:  
1. Recursion
2. Store (Memoize)
3. Bottom-up

Example: Fibonacci Sequence  
- Inefficient way (Recursion) O(2^n)
- DP (Top-down) O(n)
- DP (Bottom-up) O(n)

Java codes:

```
public class DPPractice {

    //public Map<Integer, Integer> m = new HashMap<>();
    public static int[] m;

    public static int fib(int n){
        if (n == 1 || n == 2){
            int result = 1;
            return result;
        }
        return fib(n-1) + fib(n-2);
    }

    public static int fib_dp(int n){

        m = new int[n+1];
        return fib_dp_help(n);
    }

    public static int fib_dp_help(int n){
        if (m[n] != 0){
            return m[n];
        }
        int result;
        if (n == 1 || n == 2){
            result = 1;
        } else {
            result = fib_dp_help(n - 1) + fib_dp_help(n - 2);
            m[n] = result;
        }
        return result;
    }


    public static int fib_bottom_up(int n){
        int[] f = new int[n+1];
        f[1] = 1;
        f[2] = 1;
        if (n == 1 || n ==2) return f[n];
        for(int i = 3; i <= n; i++){
            f[i] = f[i-1] + f[i-2];
        }

        return f[n];
    }

    static public void main(String[] args){
        //System.out.println(fib(1000));
        //System.out.println(fib_dp(100000));
        System.out.println(fib_bottom_up(100000));
    }
}
```