# blind75-js

## Array

### Two Sum - Easy

https://leetcode.com/problems/two-sum/

> use map, store all element as key and index as value, check if diff in map, return current and stored diff index.

```javascript
/**
 * @param {number[]} nums
 * @param {number} target
 * @return {number[]}
 */
var twoSum = function (nums, target) {
  let map = new Map();
  for (let i = 0; i < nums.length; i++) {
    let curr = nums[i];
    let diff = target - nums[i];
    if (map.has(diff)) {
      return [map.get(diff), i];
    } else {
      map.set(curr, i);
    }
  }
};
```
