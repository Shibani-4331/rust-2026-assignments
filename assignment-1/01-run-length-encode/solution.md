# Solution notes: Run-length encode

## Approach

Iterated through the input string using chars(). 
Tracked the current character and its count. 
When a different character was encountered, pushed the current (char, count) pair into the result vector and started a new run. 
Finally, pushed the last run after the loop.


## Edge cases handled
Empty input string returns an empty vector.
Single-character input returns a single (char, 1) pair.
Consecutive runs of different lengths are handled correctly.

## Anything special

Used "if let Some(curr_char) = chars.next()" to safely initialize the first run and avoid indexing into the string
