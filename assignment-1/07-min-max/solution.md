# Solution notes: `min_max`

## Approach
Return None if the slice is empty. Otherwise, initialize both min and max with the first element of the slice. 
Iterate through the slice once, updating min whenever a smaller value is found and updating max whenever a larger value is found. 
Return the final (min, max) pair.

## Edge cases handled
Empty slice returns None.
Single-element slice returns that value as both the minimum and maximum.
Handles duplicate values correctly.
Works with negative numbers as well as positive numbers.

## Anything special

