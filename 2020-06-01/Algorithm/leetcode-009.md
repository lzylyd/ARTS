## leetcode-009

回文数判断  

解题思路



```java
//思路1 求余 然后双指针遍历 时间复杂度为O(3/2n)
public static boolean isPalindrome(int x) {
            if (x < 0) {
                return false;
            }
            if (x < 10) {
                return true;
            }
            if (x % 10 == 0) {
                return false;
            }
            ArrayList<Integer> store = new ArrayList<>();
            while (x / 10 > 0) {
                store.add(x % 10);
                x = x / 10;
            }
            store.add(x);
            for (int i = 0; i < store.size() / 2; i++) {
                if (!store.get(i).equals(store.get(store.size() - 1 - i))) {
                    return false;
                }
            }
            return true;
        }
//思路2 求余同时构建reverse 时间复杂度为O(n) 且除了temp和reverse两个Int 无额外内存开销
public static boolean isPalindrome(int x) {
            if (x < 0) {
                return false;
            }
            if (x < 10) {
                return true;
            }
            int temp = x;
            int reverse = 0;
            while (x / 10 > 0) {
                reverse = reverse * 10 + x % 10;
                x = x / 10;
            }
            reverse = reverse * 10 + x;
            return reverse == temp;
        }

```

