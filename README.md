# interview-dsa

### 1.Reverse the string without reversing its individual words. Words are separated by dots.

#### First solution
```<language identifier>
  function reverseStr(str) {
  let arrStr = str.split(".");
  let newReverseArr = [];

  for (let i = arrStr.length - 1; i >= 0; i--) {
    newReverseArr.push(arrStr[i]);
  }
  return newReverseArr.join(".");
}
const result = reverseStr("i.like.this.program.very.much");
console.log(result);
```
#### Second solution
```<language identifier>
function reverseStr(str){
   arrStr = str.split(".");
   var newReveseArr = [];
   for(let i = 0; i<= arrStr.length -1;i++){
      newReveseArr[i] = (i!=0)?'.'+arrStr[arrStr.length - i - 1] : arrStr[arrStr.length - i - 1];
   }
      return newReveseArr.join("");
 }
 
  const result = reverseStr("i.like.this.program.very.much");
  console.log(result); 

```

### 2.Given a string without spaces, the task is to remove duplicates from it.
```<language identifier>
function removeDuplicates(str){
   arrStr = str.split("");
   var arr = [];
   for(let i = 0; i <= arrStr.length;i++){
     if(!arr.includes(arrStr[i])){
       arr.push(arrStr[i])
     }
   }
      return arr.join("");
 }
 
 const result = removeDuplicates("zvvaao");
 console.log(result); 
```

### 3.const obj = {test :"anirudh", test2 :{test3 :"rahul", test4 :{text5 :"alex"}}}
 output = ["anirudh", "rahul","alex"]

```
 const obj = {test :"anirudh", test2 :{test3 :"rahul", test4 :{text5 :"alex"}}}
 output = ["anirudh", "rahul","alex"]
   let stack = []; 
 function objFunction(obj){
    for(let val in obj){
      if(typeof obj[val] ==='object'){
        objFunction(obj[val])
      }else{
       stack.push(obj[val])
      }
    }
     return stack
 }
 
  const result= objFunction(obj);
  console.log(result);
```

### 4.Cumulative Sum
Arr:    [1, 2, 3, 4]
result: [1, 3, 6, 10]


```
 function cumulativeSum(arr){
   let stack =[];
   let sum = 0;
  for(let i=0; i< arr.length;i++){
     sum += arr[i]
     stack.push(sum)
  } 
  return stack;
 }

const result  = cumulativeSum([1, 2, 3, 4])
console.log(result);
```


### 5.JavaScript Program to Check an Array is Sorted or Not

```
function isArrSorted(arr) {
 for(let i= 0; i < arr.length; i++){
    if(arr[i] > arr[i + 1]){
    return false
    }
 }
   return true
}

const result = isArrSorted([1,2,3,7, 1])
console.log(result);
```

### 6.Javascript Program to Move all zeroes to end of array
Input :  arr[] = {1, 2, 0, 4, 3, 0, 5, 0};
Output : arr[] = {1, 2, 4, 3, 5, 0, 0}

```
function movezeroAtEnd(arr) {
  let zeroArr =[];
  for(let i = 0; i < arr.length; i++ ){
   if(arr[i] === 0){
    zeroArr.push(arr[i])
   }
  }
  let filterArr = arr.filter(item => item !== 0);
  return filterArr.concat(zeroArr);
}

const result = movezeroAtEnd([1, 2, 0, 4, 3, 0, 5, 0])
console.log(result);
```

```
function movezeroAtEnd(arr) {
  let zeroArr =[];
  let zeroCount =0;
  for(let i = 0; i < arr.length; i++ ){
   if(arr[i] === 0){
    zeroCount++;
   }else {
    zeroArr.push(arr[i])
   }
  }
  
  while(zeroCount > 0){
    zeroArr.push(0);
    zeroCount--
  }
   return zeroArr;
}

const result = movezeroAtEnd([1, 2, 0, 4, 3, 0, 5, 0])
console.log(result);
```

### 7. Map and their Polyfills
const employees = [
    { name: 'John', age: 32 },
    { name: 'Sarah', age: 28 },
    { name: 'Michael', age: 40 },
];

 const employessName = employees.map((item)=>{
  return item.name;
})
console.log(employessName);


```
//Polyfills



```

### 8. How to count string occurrence in string (hashmap).

```
function count(str) {
  const strArr = str.split(" ");
  let wordcount ={}
  for(let i =0; i < strArr.length; i++){
    let word = strArr[i];
    if(wordcount[word]){
       wordcount[word]++;
    }else {
      wordcount[word] = 1
    }  
  }
   return wordcount;
}

const result = count("hi hllo hlo anirudh anirudh ji hi ji hi");
console.log(result);
```


### 9. Merge Two Sorted Arrays and  remove the dublicate value.
A: [1, 2, 3, 4, 4]
B: [2, 4, 5, 5]
C: [1, 2, 2, 3, 4, 4, 4, 5, 5]

```

 function sortArr(arr1, arr2){
   const margeArr =  [...arr1, ...arr2];
    const newArr =[];
     for(let i= 0; i < margeArr.length; i++){
       if(!newArr.includes(margeArr[i])){
         newArr.push(margeArr[i])
       }
     }
      return newArr;
 }
 const result = sortArr([1,2,3,4,5,5,6], [3,4,4,5,6,7,7,7]);
 console.log(result); 
```


### 10. Find a pair with the given sum in an array.

```
function sumofThePair(arr, target) {
const pairs = [];
   for(let i= 0; i < arr.length; i++){
    for(let j= i + 1; j < arr.length; j++){
       if(arr[i] + arr[j] === target){
          pairs.push([arr[i], arr[j]]);
       }
    }
   }
   return pairs.length ? pairs : null; 
}
  
  
  const arr = [6, 0, 8, 2, 3, 0, 4, 0, 1 ];
  const result =  sumofThePair(arr, 10);
  console.log(result) 
```

### 11. Sorting 

### Bubble short

```
function bubbleSort(arr) {
 for(let i= 0 ; i <arr.length; i++){
    for(let j = 0; j < (arr.length - i -1); j++) {
       if(arr[j] > arr[j+1]){
         var temp = arr[j];
         arr[j] = arr[j + 1]
         arr [j+1] = temp;
       }
    }
 }
 return arr
}
  
  
  const arr = [6, 0, 8, 2, 3, 0, 4, 0, 1 ];
  const result =  bubbleSort(arr);
  console.log(result)

```
Optimized Solution

```
function bubbleSort(arr) {
let isSwapped;
 for(let i= 0 ; i <arr.length; i++){
  isSwapped = false;
    for(let j = 0; j < (arr.length - i -1); j++) {
       if(arr[j] > arr[j+1]){
         var temp = arr[j];
         arr[j] = arr[j + 1]
         arr [j+1] = temp;
          isSwapped = true;
       }
    }
  if (!isSwapped) 
            break;
 }
 return arr
}
  
  
  const arr = [6, 0, 8, 2, 3, 0, 4, 0, 1 ];
  const result =  bubbleSort(arr);
  console.log(result) 

```


### 12. Can you write a function in JavaScript to remove duplicate elements from an array?

```
 function removeDublicalte(arr){
   let temp =[];
   for(let i =0; i < arr.length; i++){
    if(!temp.includes(arr[i])){
     temp.push(arr[i])
    }
   }
   return temp;
 }
 
const result = removeDublicalte([1,2,3,4,5,4,3,2]);
console.log(result);
```

### 13. Can you write a function in JavaScript to get the current date in the format “YYYY-MM-DD”?

```
 function currDate(){
   return new Date().toISOString().split('T')[0];
 }
 
  const result = currDate();
  console.log(result);
```
### 14. Can you write a function in JavaScript to split an array into chunks of a specified size?

```
 function chunkArray(arr, chunkSize){
  
  let result =[];
  for (let i = 0; i < arr.length; i += chunkSize) {
     console.log(i + chunkSize)
    result.push(arr.slice(i, i + chunkSize));
  }
   return result
  
 }

const chunkedArray = chunkArray([1,2,3,4,5,6,7,6,5], 3);
  console.log(chunkedArray);

```
### 15. Find a pair with the given sum in an array?

```
function sumOfTwo(arr, target) {
  const pairs = []; 

  for (let i = 0; i < arr.length; i++) {
    for (let j = i + 1; j < arr.length; j++) {
      if (arr[i] + arr[j] === target) {
        pairs.push([arr[i], arr[j]]); 
      }
    }
  }

  return pairs; 
}

const result = sumOfTwo([8, 7, 2, 5, 3, 1], 10);
console.log(result); 
```

### 16. multiplay the value of  array  with Recursion?

```
  function multiplayFun(arr) {
    if(arr.length <= 0){
    return 1
    }else{
     return arr[arr.length -1 ] *  multiplayFun(arr.slice(0, arr.length -1 )) 
    }
  }
  const result = multiplayFun([1,2,3,4,5]);
  console.log(result);
```

### 17. Factorial of a Number with Recursion?

```
 function Factorial(num){
  if(num <= 0){
  return 1;
  }else{
    return num * Factorial(num - 1);
  }
 }
 
 const result = Factorial(0);
 console.log(result)
```

### 18.Reverse a String  with Recursion?

```
 function ReverseString(str){
    if(str.length <= 0){
    return str
    }else{
    return ReverseString(str.slice(1)) + str[0];
    }    
   
 }
 const result = ReverseString("myname");
 console.log(result);
```

### 19. Check Palindrome (Recursion)?

```
 function isPalindrome(str){
    if(str.length <= 1){
    return true
    }
    
     if(str[0] !== str[str.length - 1]){
       return  false
     }    
     return isPalindrome(str.slice(1, -1))   
 }

 const result = isPalindrome("madame");
 console.log(result);
```
### 20.Count Vowels in a String ?

```
 function countVowels(str){
  let vowels = ["a", "e", "i","o", "u"];
  let strArr = str.toLowerCase().split("");
 return strArr.filter(char => vowels.includes(char)).length;
  
 }

 const result = countVowels("aaaaaaa");
 console.log(result);
```

### 21. Find the frequency of elements in array ?

```

 function frequenyWord(arr){
  const temp = {};
    arr.forEach((item)=>{
     if(temp[item]){
       temp[item]++
     }else{
     temp[item] = 1
     }
    })
    
   return temp
 }

 const result = frequenyWord(["laptop", "word", "sofa", "word"]);
 console.log(result)
```

### 22.  Group items on the basis of age of given array of object?

```
 function groupByAge(data){
   const check = {};
   data.forEach((item)=>{
    if(!check[item.age]){
        check[item.age] = [item]
    }else {
        check[item.age].push(item)
    }
   })
   return  check
 }

 const result = groupByAge([{name  :"anirudh", age  :25}, {name  :"abin", age :21}, {name : "rehan" , age : 25}]);
 console.log(result)
```

### 23. Simple Queue

```
class Queue {
    constructor() {
        this.items = [];
    }

    enqueue(element) {
        this.items.push(element); 
    }

    dequeue() {
        if (this.isEmpty()) {
            return "Underflow, cannot perform dequeue";
        }
        return this.items.shift(); 
    }

    isEmpty() {
        return this.items.length === 0; 
    }

    front() {
        if (this.isEmpty()) {
            return "No element in the queue";
        }
        return this.items[0]; 
    }

    size() {
        return this.items.length; 
    }

    printQueue() { 
        let queueString = "";
        for (let i = 0; i < this.items.length; i++) {
            queueString += this.items[i] + ", "; 
        }
        console.log("Queue:", queueString.slice(0, -2)); 
    }
}

const myQueue = new Queue();
myQueue.enqueue(5);
myQueue.dequeue();
myQueue.enqueue(10);
myQueue.enqueue(20);
console.log(myQueue.front());
console.log(myQueue.size());
myQueue.printQueue(); 

```

### 23. Circular Queue?

```
function myCircularQueue(k) {
   this.queue = [];
   this.size = k;
}

myCircularQueue.prototype.enqueue = function (value){
if(this.size === this.queue.length) {
return  false;
}
 this.queue.push(value);
 return true;
}


myCircularQueue.prototype.dequeue = function (){
if(this.queue.length === 0 ) return false;
 this.queue.shift();
 return true;
}

myCircularQueue.prototype.front = function (){
 if(this.queue.length === 0 ) return -1;
 return this.queue[0];
}

myCircularQueue.prototype.rear = function (){
 if(this.queue.length === 0 ) return -1;
 return this.queue[this.queue.length - 1];
}

myCircularQueue.prototype.isFull = function (){
if(this.size === this.queue.length) {
return  false;
}
return true
}

var obj = new myCircularQueue(3);
var params_1 = obj.enqueue(1);
var params_1 = obj.enqueue(3);
var params_1 = obj.enqueue(4);
console.log(obj.front(), obj.rear());
```






