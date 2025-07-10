## 1480. Running Sum of 1D Array

Give an array `nums`. We define a running sum of an array as `runningSum[i] = sum(nums[0]...nums[i]).

return the running sum of `nums`.

### My pseudocode:

Create a variable called `a` to store values.
Iterate over each element in the array adding each value to the `a` variable. 
At each point in the array, change to current value of `a`.

-----

### Python

#### My answer
```
class Solution(object):
    def runningSum(self, nums):
        """
        :type nums: List[int]
        :rtype: List[int]
        """
        # Set variable to store value.
        a = 0

        # Iterate over each element in the array adding to a and replacing value in the array.
        for i in range(len(nums)):
            a+=nums[i]
            nums[i] = a
        return nums
```