# Computer_Graphics_Assignments
## Bresenham's Line Algorithm Implementation in Python
This repository contains Python code implementing Bresenham's Line Drawing Algorithm with adjustments specifically for the case where the slope (m) of the line is greater than 1.
### Adjustments for m>1:
In the original Bresenham's Line Drawing Algorithm, the decision parameter calculation and pixel selection are based on the change in the x-coordinate.
However, when m>1, the algorithm needs to consider the change in the y-coordinate instead of the x-coordinate.The modification is needed because the line is steeper in the vertical direction than in the horizontal direction.
The modification involves :
+ **Swapping Coordinates:** The X and Y coordinates of the input points are swapped.
+ **Decision Parameter Modification:** The best case for decision parameter (d) is adjusted to d_new = 2 * dx - dy  and for general case, decision parameter (d) is adjusted to d_new = d + 2 * dx - 2 * dy
  
####For Case 1: (1,1),(8,4)
+ **Slope :** m=(4-1)/(8-1)=3/7<1
+ **Intermediate Coordinates:** (1, 1), (2, 1), (3, 2), (4, 2), (5, 2), (6, 3), (7, 3), (8, 4)
+ **Decision Variables:**  -1, 5, -3, 3, -5, 1, -7, -1
+ **Figure:** 

