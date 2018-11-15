# Cats and a Mouse

## Problem
https://www.hackerrank.com/challenges/cats-and-a-mouse/problem

## solve (javascript)
```javascript
function catAndMouse(x, y, z) {   
    
    const result = Math.abs(x-z)< Math.abs(y-z) 
                    ? "Cat A" 
                    : (Math.abs(x - z) > Math.abs(y-z) ? "Cat B" : "Mouse C");    
        
   return result;
    
}
