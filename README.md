# Problem Description
1. A 3D matrix is to be stored in a 1D vector (flattened)
2. The 3D matrix is of size n x m x p and is indexed by i, j, k
3. The 1D vector is of size q and is indexed by y
# Requirements
Implement the following functions:
1. Create a 1D vector suitable for storing the 3D matrix
2. Convert the 3D matrix index (i, j, k) to a suitable 1D vector index (y). Must be O(1)

# Solution 
3d array is just an array of `2d arrays`, to convert 2d array to 1d array 
we calculte 2d array idx = weight*rowI + colJ
what we will do in the 3d array case ? 

Solution is prety simple all i need is to know to total indexes or the first index in my 2d array for example :

![Whiteboard](https://github.com/amrhossamdev/Matrix-Flatten/blob/main/whiteboard.png)

i need to calculte indecies for that 2d array ! 
1. First i need to know the last previous index it will be equal to = `7` then i will increment it by 1 to get first index in the 2d array i'm in !
2. i need to calculte the index `for pos [2,1,0]` so i know my `previous index was 7` and `my first 2d array index is 8` 
3. so the answer will be `8 + [current 2d array idx] = w*rowJ + colI = 2*1 + 0 == 8 + 2 == 10 !` 

# Used algorithm

1. `2d array idx = width * row + col`
2. `3d array idx = (width * height * i) + [2d array idx]`

finally -> `int idx = (m * p * i) + (m * j) + k;`

# Example 
![Whiteboard](https://github.com/amrhossamdev/Matrix-Flatten/blob/main/result.png)


