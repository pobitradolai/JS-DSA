# JS-DSA

> [!NOTE]
> Useful information that users should know, even when skimming content.
>
> 
```
dsa-js/
├── arrays/
├── linked-lists/
├── stacks-queues/
├── recursion/
├── sorting/
├── trees/
├── graphs/
└── dp/
```
## Reverse an Array
```
function reverseArray(arr) {
  let left = 0;
  let right = arr.length - 1;

  while (left < right) {
    [arr[left], arr[right]] = [arr[right], arr[left]]; // Swap
    left++;
    right--;
  }

  return arr;
}

console.log(reverseArray([1, 2, 3, 4, 5])); // [5,4,3,2,1]

```

## Find the Maximum Element
```
function findMax(arr) {
  let max = arr[0];

  for (let i = 1; i < arr.length; i++) {
    if (arr[i] > max) max = arr[i];
  }

  return max;
}

console.log(findMax([3, 1, 7, 9, 4])); // 9

```
## Check if Array is Palindrome
```
function isPalindrome(arr) {
  let left = 0, right = arr.length - 1;
  while (left < right) {
    if (arr[left] !== arr[right]) return false;
    left++;
    right--;
  }
  return true;
}

console.log(isPalindrome([1, 2, 3, 2, 1])); // true
console.log(isPalindrome([1, 2, 3]));       // false

```
## Move All Zeros to the End
```
function moveZeros(arr) {
  let insertPos = 0;

  for (let i = 0; i < arr.length; i++) {
    if (arr[i] !== 0) {
      arr[insertPos++] = arr[i];
    }
  }

  while (insertPos < arr.length) {
    arr[insertPos++] = 0;
  }

  return arr;
}

console.log(moveZeros([0, 1, 0, 3, 12])); // [1, 3, 12, 0, 0]

```
## remove Duplicates 
```
function removeDuplicates(arr) {
    if(arr.length === 0) return 0;

    let i = 0;
    for (let j = 1; j < arr.length; j++) {
        if (arr[i] !== arr[j]) {
            i++;
            arr[i] == arr[j]
        }
    }
    return arr.slice(0, i + 1)
}

console.log(removeDuplicates([1, 2, 3, 4, 5, 5]))  // [1, 2, 3, 4, 5]


```

## 
