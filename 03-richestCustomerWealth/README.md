**Challenge**

You are given an m x n integer grid accounts where accounts[i][j] is the amount of money the i​​​​​​​​​​​th​​​​ customer has in the j​​​​​​​​​​​th​​​​ bank. Return the wealth that the richest customer has.

A customer's wealth is the amount of money they have in all their bank accounts. The richest customer is the customer that has the maximum wealth.
**Solution:**

```js
var maximumWealth = function(accounts) {

    let maxWealth=0;
    accounts.map((account, key)=>{
        let sum=0;
        account.forEach(money=>{
            sum+=money;
        })

        if(sum>maxWealth)
            maxWealth=sum;
    })
    return maxWealth;

};
maximumWealth([[1,2,3],[3,2,1]]);//Will return 6
```

**Explanation**

At each iteration we sum all the amounts each customer owns and compare that with maxWealth variable. At the end of the function we return the highest wealth owned by a particular customer.

[Leet Code Submission](https://leetcode.com/problems/richest-customer-wealth/submissions/974793773/)