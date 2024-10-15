## Remove Dublicate Array
```javascript
function removeDublicateArr(arr) {
  var uniqueArr = [];
  for(var i = 0; i < arr.length; i++) {
    if(uniqueArr.indexOf(arr[i]) === -1) {
      uniqueArr.push(arr[i]);
    }
  }
  return uniqueArr;
}
var arr = [1,2,3,5,1,4,6,2,4,5,7,2,5]
var result = removeDublicateArr(arr);
console.log(result);
output = [1,2,3,4,5,6,7]
```

## Explenation 
**1. Function Definition:** <br>
removeDuplicates(arr) takes an array arr as input.

**2. Unique Array Initialization:** <br>
uniqueArr is an empty array to store unique elements.

**3. For Loop:** <br>
Iterates over each element in arr.

**4. Check for Duplicates:** <br>
indexOf(arr[i]) === -1 checks if the element is already in uniqueArr.

**5. Add Unique Element:** <br>
If the element isn't found, it is added to uniqueArr using push().

**6. End of Loop:** <br>
Loop and if block are closed.

**7. Return Unique Array:** <br>
After the loop, uniqueArr (containing only unique elements) is returned.
