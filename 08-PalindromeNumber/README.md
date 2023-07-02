**Challenge**

Given an integer x, return true if x is a palindrome, and false otherwise.
**Solution:**

```js
/**
 * @param {number} x
 * @return {boolean}
 */
var isPalindrome = function (x) {

        let chars = x.toString().split("");
        let left = 0;
        let right = chars.length - 1;
        while (left < right) {
            if (chars[left] !== chars[right])
                return false;

            right--;
            left++;
        }
        return true;
    };
```

[Leet Code Solution](https://leetcode.com/problems/palindrome-number/submissions/984631184/)