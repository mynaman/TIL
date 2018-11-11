# Sock Merchant

## Problem
https://www.hackerrank.com/challenges/sock-merchant/problem

## solve (javascript)
```javascript
function sockMerchant(n, ar) {
    const map = new Map();
    let pairs = 0; 
    
    ar.forEach((v, i) => {
        !map.has(v) ? map.set(v, 1) : map.set(v, map.get(v) + 1);
    });
    
    map.forEach((v, i) => {
        pairs += v !== 1 ? ( v % 2 === 0 ? v : v - 1 ) : 0;
    });
    
    return pairs / 2;
}
