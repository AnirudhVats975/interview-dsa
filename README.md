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

### 7.Map and their Polyfills
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





