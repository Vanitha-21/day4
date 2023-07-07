# day4
a).
//anonymous function
let arr=[0,1,2,3,4,5,6,7,8,9];
let odd=function (){
  let odd= arr.filter(num => num %2 ==1)
  console.log(odd)
}
odd()
out put: [1,3,5,7,9]

//IIFS function
let a=[0,1,2,3,4,5,6,7,8,9];
(function () {
  let odd= a.filter(num => num %2 ==1);
  return odd;
})();
out put:[1,3,5,7,9]


b).
//anonymous function
let str= function () {
  let arr ="hello how are you "
  let titlecase = arr.toLowerCase().replace(/\b(\w)/g, s => s.toUpperCase());
  console.log(titlecase)
}
str()
output:
HELLO HOW ARE YOU

//IIFE Function
(function (str) {
  str = str.toLowerCase().split(' ');
  for (var i = 0; i < str.length; i++){
    str[i] = str[i].charAt(0).toUpperCase() + str[i].slice(1);
  }
  console.log(str.join(' '));
})("hello how are you")
output:
HELLO HOW ARE YOU

c).
//anonymous
let func = function () {
  let ar = [1,2,3,4,5]
  let sum = ar .reduce(function(a,b){
    return a + b;
  });
  console.log(sum);
}
func()
output:
15

//IIFE
(function () {
  let sum = [1,2,3,4,5].reduce(add, 5);
  function add(accumulator, a) {
    return accumulator + a;
  }
  console.log(sum);
})()
output:
20

d).

//anonymous
let prime = function (arr) {
  return arr.filter (function(n){
    for (let i = 2; i < n; i++) {
      if (n % i === 0) return false;
    }
    return n > 1;
  });
};
console.log(prime([7,16,9,3]));

outpt:
[7,3]

//IIFE:
(function (){
  var primeNum = [7,16,9,3]
  primeNum = primeNum.filter(function(number) {
    for (var i =2; i <= Math.sqrt(number); i ++) {
    if (number % i == 0) return false;
  }
  return true;
});
console.log(primeNum);
})()

output:
[7,3]

e).

//anonymous
let isPalindrome = function () {
  var myArray = ['vani', 'anu', 'rishi', 'bharath kumar'];
  var arr = myArray.filter(function (c, d) {
    var Palindrome = c.split('').reverse().join('');
    if (c == Palindrome) {
      console.log(myArray[d]);
    }
  });
}
isPalindrome()

output:
anu bharath kumar


//IIFE
( function () {
  var myArray = ['vani','anu','rishi','bharath kumar'];
  var arr = myArray.filter(function (c,d) {
    var palindrome = c.split('').reverse().join('');
    if (c == palindrome) {
      console.log(myArray[d]);
    }
  });
})()
  

output:
anu bharath kumar

f).
//anonymous
let median = function(a,b) {
  let c = [...a,...b]. sort((a,b) => a-b);
  const half = c.lenth /2 | 0;
  if (c.lenth %2) {
    return c[half];
  }else{
    return (c[half] + c[half - 1]) / 2;
  }
}
let arr1 = [1,12,15,26.38,24];
let arr2 = [2,13,17,30,45,47];
console.log(median(arr1,arr2));

output:
20.5

//IIFE
(function(){
  let arr1=[1,12,15,26,38,24];
  let arr2=[2,13,17,30,45,47];
  let c=[...arr1,...arr2].sort((arr1,arr2) =>arr1 - arr2);
  const half = c.length/2 |0;
  if (c.length % 2) {
    console.log(c[half]);
  }else{
    console.log((c[half] + c[half - 1]) / 2);
  }
})()
 
  
output:
20.5

h).
//anonymouse
let findDuplicates = function(){
  const yourArray = [1,1,2,3,4,5,5]
  let duplicates=[]
  const tempArray = [...yourArray].sort()
  for (let i =0; i<tempArray.length; i++){
    if (tempArray[i + 1] ===tempArray[i]){
      duplicates.push(tempArray[i])
    }
  }
  console.log(duplicates)
}
findDuplicates()

output:
1 5

//IIFE
(function () {
  let number =[1,1,3,2,4,5,5,6];
  let duplicates= numbers.filter((item, index) => index !== numbers.indexOf(item));
  console.log(duplicates);
})()

output:
1 5

h).
//anonymous
let rotateArray = function(A,K) {
  if (A.length === K || K=== 0) {
    return A;
  }
  K = K%A.length;
  for (let i=0; i<K; i++) {
    A. unshift(A. pop());
  }
  console.log(A)
}
rotateArray([1,2,3,4,5],2)

output:
[4, 5, 1, 2, 3]

//IIFE
(function(A, K) {
  if (A.length === K || K === 0) {
    return A;
  }
  K = K % A.length;
  for (let i =0; i <K; i++) {
    A. unshift(A. pop());
  }
  console.log(A)
})([1,2,3,4,5],2)

output:
[4, 5, 1, 2, 3]


