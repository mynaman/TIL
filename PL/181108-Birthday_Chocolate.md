# Breaking the Records

## Problem
https://www.hackerrank.com/challenges/the-birthday-bar/problem

## solve (javascript)
```javascript
function birthday(s, d, m) {    
    let counter = 0, sum = 0;  
    
    for(let i=0; i< s.length; i++) {
        for(let j=i; j<i+m; j++) {
            sum += s[j];
        }        
        counter += (sum === d) ? 1 : 0;
        sum = 0;
    }    
    return counter;
}
