# Solution notes: Split and double

## Approach

Use split_at_mut(mid) to split the vector into two disjoint mutable slices. 
Iterate through each slice and double every element in place. Return the two mutable slices.

## Edge cases handled
mid == 0: the left slice is empty and the right slice contains all elements.
mid == xs.len(): the right slice is empty and the left slice contains all elements.
Empty vectors are handled correctly.
mid > xs.len() panics automatically through split_at_mut, as required.

## Anything special
The key idea is using split_at_mut, which allows two non-overlapping mutable borrows of the same vector.
