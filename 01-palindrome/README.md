**Challenge**

Check if the string is a palindrome. 
A palindrome is a string that is spelt same from left to right and right to left e.g Dad, Mom. 

Write a function to check if the string is a palindrome.

**Solution:**

```js 
function isPalindrome(string)
{
    //Empty strings are considered palindromes as well
    if(string===null||string===undefined||string==='')
     return true;
     
     //We convert the letters to lowercase as we just need to check if letter is same irrespective of case
     let stringChars=string.toLowerCase().split('');
     
     //Iterating the string from front and back and checking if letters are same on each iteration
     for(let i=0;i<stringChars.length-1;i++)
     {
       if(stringChars[i] !== stringChars[stringChars.length-(i+1)])
       return false;
     }
     return true;
}

isPalindrome('tenet');//returns true;
isPalindrome('dad');//returns true;
isPalindrome('Github');//returns false;

```
**Explanation**

To approach the problem we simply convert the string into characters and iterate over the string from left to right and right to left at the same time. At each iteration the letters need to be same, as per the definition of palindrome. If they are same then complete string is palindrome otherwise it is not.
