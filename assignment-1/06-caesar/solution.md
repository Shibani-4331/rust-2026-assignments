# Solution notes: Caesar cipher

## Approach

Iterate through each character in the input string. 
For alphabetic characters, determine their position in the alphabet, apply the shift, and wrap around when the position goes past the beginning or end of the alphabet. 
Preserve the original letter case. Non-alphabetic characters are copied to the output unchanged.

## Edge cases handled
Negative shifts.
Shifts larger than the alphabet length.
Uppercase and lowercase letters.
Digits, punctuation, and whitespace remain unchanged.
Empty input strings return an empty string.

## Anything special

Wrapping is implemented by adjusting positions back into the valid range whenever they go below 0 or above the alphabet length.
