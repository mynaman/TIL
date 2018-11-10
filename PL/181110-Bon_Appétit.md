# Bon Appétit

## Problem
https://www.hackerrank.com/challenges/bon-appetit/problem

## solve (javascript)
```javascript
function bonAppetit(bill, k, b) {
    const half = bill.filter((v, i) => i != k).reduce((a, c) => a + c) / 2;    
    const result = b > half ? b-half : 'Bon Appetit';
    
    console.log(result);
}
