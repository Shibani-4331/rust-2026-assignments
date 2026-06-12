# Solution notes: Longest word slice

## Approach

Split the sentence into whitespace-separated words, then iterate through them while tracking the longest word seen so far. Return a borrowed slice to the longest word, or None if no words are present.

## Edge cases handled

-Empty space and whitespaces only, return None
-if more than one word exist with same length then the first one is returned

## Anything special

No String allocation occured