# Solution notes: Censor vowels in place

## Approach

Iterate through the string's characters using chars(). 
For each character, replace it with '*' if it is an ASCII vowel . 
Collect the transformed characters into a new String and assign it back to the original mutable string.

## Edge cases handled
Empty strings remain unchanged.
Strings without vowels are left unchanged.
Both uppercase and lowercase vowels are censored.

## Anything special

This solution uses a safe approach with chars(), map(), and collect() instead of mutating the string's bytes directly.