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
