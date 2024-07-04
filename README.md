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
