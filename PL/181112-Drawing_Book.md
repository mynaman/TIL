# Drawing Book

## Problem
https://www.hackerrank.com/challenges/drawing-book/problem

## solve (javascript)
```javascript
function pageCount(n, p) {  
    n = Math.floor(n/2);
    p = Math.floor(p/2);
    const count = Math.min(p, n-p);
    return count;
}
