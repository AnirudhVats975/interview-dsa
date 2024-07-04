# interview-dsa

### 1.Reverse the string without reversing its individual words. Words are separated by dots.

```<language identifier>
 function reverseStr(str){
   arrStr = str.split(".");
   var newReveseArr = [];
   for(let i = 0; i<= arrStr.length;i++){
      newReveseArr[i] = arrStr[arrStr.length - i - 1];
   }
      return newReveseArr.join(".");
 }
 
  const result = reverseStr("i.like.this.program.very.much");
  console.log(result);

```
