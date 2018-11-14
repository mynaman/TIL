# Counting Valleys

## Problem
https://www.hackerrank.com/challenges/counting-valleys/problem

## solve (javascript)
```javascript
function countingValleys(n, s) {
    let num = 0;
    let updown = 0;
    
    for(let x=0; x<n; x++) {
        if(s[x] === 'U') {
            updown += 1;
        } else {
            updown -= 1;
        }        
        if(updown === 0 & s[x] === 'U') num++;
    }
    
    return num;
}
