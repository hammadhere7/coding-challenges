**Challenge**

Given an integer array nums, return true if any value appears at least twice in the array, and return false if every element is distinct.


**Solution:**

```js
var containsDuplicate = function(nums) {

    let numSet=new Set();

    for(let i=0; i<nums.length;i++)
    {
        if(!numSet.has(nums[i]))
            numSet.add(nums[i]);
        else
            return true;
    }
    return false;

};
containsDuplicate([1,5,3,7,8,2,9,4]);//Will false as every element is distinct
```

[Leet Code Solution](https://leetcode.com/problems/contains-duplicate/submissions/978410025/)