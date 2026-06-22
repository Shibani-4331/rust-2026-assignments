# Solution notes: Character frequency, sorted

## Approach

Used a HashMap to count the frequency of each character in the input string. 
Then converted the hashmap into a vector of pairs and sorted it by frequency in descending order. 
If two characters have the same frequency, they are sorted alphabetically.

## Edge cases handled
Empty input string returns an empty vector.
Single-character strings.
Strings where all characters have the same frequency.
Spaces and other non-letter characters are counted as well.

## Anything special

The solution uses a HashMap for efficient frequency counting and a custom sort to satisfy the required output ordering.
