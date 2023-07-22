**Challenge**

Given an input string `s`, reverse the order of the words.

A word is defined as a sequence of non-space characters. The words in s will be separated by at least one space.

Return a string of the words in reverse order concatenated by a single space.

Note that `s` may contain leading or trailing spaces or multiple spa

**Solution:**

```js
/**
 * @param {string} s
 * @return {string}
 */
var reverseWords = function(s) {

        s=s.trim();
        s=s.replace(/ +/g, " ");
        let words=s.split(" ");
        let reversed="";

        for(let i=words.length;i>0;i--)
            reversed+=words[i-1]+" ";

        return reversed.trim();

    };
```

[Leet Code Solution](https://leetcode.com/problems/reverse-words-in-a-string/submissions/1000854961/)