# Damerau-Levenshtein-distance
Damerau–Levenshtein distance is a string metric for measuring the edit distance between two sequences. Informally, the Damerau–Levenshtein distance between two words is the minimum number of operations (consisting of insertions, deletions or substitutions of a single character, or transposition of two adjacent characters) required to change one word into the other. 

The restricted distance function is defined recursively as:
```
                 _
                |  0                         if i=j=0
                |  da,b(i−1,j)+1             if i>0
     da,b(i,j) <   da,b(i,j−1)+1             if j>0
                |  da,b(i−1,j−1)+1(ai≠bj)    if i,j>0
                |_ da,b(i−2,j−2)+1           if i,j>1 and a[i]=b[j-i] and a[i-1]=b[j]
```          

where 1(ai≠bj) is the indicator function equal to 0 when ai=bj and equal to 1 otherwise. 
```
  da,b(i−1,j)+1  corresponds to a deletion (from a to b).
  da,b(i,j−1)+1  corresponds to an insertion (from a to b).
  da,b(i−1,j−1)+1 (ai ≠ bj)  corresponds to a match or mismatch, depending on whether the respective symbols are the same.            
  da,b( i − 2 , j − 2 ) + 1  corresponds to a transposition between two successive symbols.
```
The Damerau–Levenshtein distance between a and b is then given by the function value for full strings: da,b(|a|,|b|) where i=|a| denotes the length of string a and j=|b| is the length of b. 
