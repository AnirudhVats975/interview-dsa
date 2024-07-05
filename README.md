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



