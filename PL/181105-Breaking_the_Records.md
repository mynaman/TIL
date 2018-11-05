# Breaking the Records

## Problem
https://www.hackerrank.com/challenges/breaking-best-and-worst-records/problem

## solve (javascript)
```javascript
function breakingRecords(scores) {
    let highest_counter = 0, lowest_counter = 0;
    let highest_score = scores[0], lowest_score = scores[0];
    for(let i=1; i<scores.length; i++) {
        if( highest_score < scores[i] ) {
            highest_score = scores[i];  
            highest_counter++;
        } 
        else if( lowest_score > scores[i] ) {
            lowest_score = scores[i];  
            lowest_counter++;
        }
    }
    return [highest_counter, lowest_counter];
}
