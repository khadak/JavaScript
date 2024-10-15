## Two Sum
**Approach 1: Brute Force**
```javascript
function twoSum(number, target) {
  for(var i = 0; i < number.lenght; i++ ) {
    for(var j = 1; j < number.length; j++) {
        if(number[i]+number[j] == target) {
          return [number[i], number[j]]
        }
    }
  }
}
```
**Approach 1: Has Table**
```javascript
function twoSum(number, target) {
  var numberToIndex = {};
  for(var i = 0;  i < number.lenght; i++) {
    var complement = target - number[i];
    if(numberToIndex.hasOwnProperty(complement)) {
      return [numberToIndex[complement], i]
    }
    numberToIndex[number[i]] = i
  }
}

```
**Definition of the Function:** This line defines a function named twoSum that takes two parameters: nums, an array of numbers, and target, the number we want to reach by summing two numbers from the nums array.

```let numToIndex = {};```<br>
**Hash Table Initialization:** Here, we initialize an empty object named numToIndex. This object will act as a hash table to store each number from the nums array as a key, and its corresponding index as the value.

**Loop Through Array:** This line starts a for loop that will iterate through each element in the nums array. The variable i serves as the index of the current element.

```let complement = target - nums[i];```<br>
**Calculate the Complement:** For the current number nums[i], we calculate the complement by subtracting nums[i] from target. The complement is the value we need to find in the hash table to complete the sum to target.

 ```if (numToIndex.hasOwnProperty(complement))```<br>
**Check for Complement:** This line checks if the complement exists in our hash table numToIndex. We use hasOwnProperty to ensure we're checking only the properties that belong to the object itself.

```return [numToIndex[complement], i];``` <br>
**Return Indices:** If the complement is found, we return an array containing the index of the complement (retrieved from numToIndex) and the current index i. This means we found two numbers that add up to the target.

```numToIndex[nums[i]] = i;```<br>
**Store Current Number:** If the complement is not found, we store the current number nums[i] in the hash table with its index i as the value. This allows us to check this number later if we encounter a new number that might complement it.
