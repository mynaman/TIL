# Migratory Birds

## Problem
https://www.hackerrank.com/challenges/migratory-birds/problema

## solve (javascript)
```javascript
function migratoryBirds(arr) {    
    const map = new Map();    
    const unique = [0,0];    
    arr.forEach((v) => !map.has(v) ? map.set(v, 1) : map.set(v, map.get(v)+1));   
    map.forEach((v, k) => { 
                            if(unique[1] < v) {
                                unique[0] = k; unique[1] = v;
                            } else if(unique[1] === v && unique[0] > k) {
                                unique[0] = k; unique[1] = v;
                            }        
                          }); 
    return unique[0];
}
