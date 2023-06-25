**Challenge**

Given a string s consisting of words and spaces, return the length of the last word in the string.

**Solution:**

```js
var lengthOfLastWord = function(s) {

        let words=s.trim().split(" ");
        lastWord=words[words.length-1];
        lastWord=lastWord.trim();
        return lastWord.length;

    };
lengthOfLastWord("Hello World ");//Should return 5
```

[Leet Code Solution](https://leetcode.com/problems/length-of-last-word/submissions/978716398/)