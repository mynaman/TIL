# Electronics Shop

## Problem
https://www.hackerrank.com/challenges/electronics-shop/problem

## solve (javascript)
```javascript
function getMoneySpent(keyboards, drives, b) {
    const k_length = keyboards.length;
    const d_length = drives.length;
    let result = 0;
    
    for(let i=0; i< k_length; i++) {
        for(let y=0; y< d_length; y++) {
            let total = keyboards[i] + drives[y];            
            result = ((result <= total) && total <= b) ? total : result;
        }
    }    
    return result === 0 ? -1 : result;
}
