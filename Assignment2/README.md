# clean-code-assignments

2.Use whitespace for readability: Use whitespace to break up your code into logical sections, making it easier to read and understand. For example:

```
// Bad

for(let i=0;i<10;i++){

  console.log(i);

}

// Good

for (let i = 0; i < 10; i++) {

  console.log(i);

}
```

Question : Given an array nums containing n distinct numbers in the range [0, n], return the only number in the range that is missing from the array.

```

Input: nums = [3,0,1]
Output: 2
Explanation: n = 3 since there are 3 numbers, so all numbers are in the range [0,3]. 2 is the missing number in the range since it does not appear in nums.


Constraints:

n == nums.length
1 <= n <= 104
0 <= nums[i] <= n
All the numbers of nums are unique.
```
