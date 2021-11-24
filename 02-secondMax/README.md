**Challenge**

Given an unsorted array of integers, the job is to find the second maximum element in the array.
Constraint for that is you cannot sort the array. The provided solution must solve it without sorting the array.

**Solution:**

```js
function secondMax(numbers){

  //We will assume that both max and second max are negative infinite numbers  
  let max=-Infinity;
  let secondMax=-Infinity;

  numbers.forEach(number=>{
      if (number > max) {
        secondMax=max;
        max=number;
      } else if (number < max && number > secondMax) {
        secondMax = number;
      }
    
  });
  return secondMax;

}
secondMax([1,5,3,7,8,2,9,4]);//Will return 8
```

**Explanation**

At each iteration we check that if the number is greater than previous maximum number stored. If that is the case then we save new maximum number in max variable and save old maximum number in secondMax variable. If the number is less than max and greater than secondMax then we just update the secondMax with that number.

[Repl Link](https://replit.com/@hammadhere10/secondMax)