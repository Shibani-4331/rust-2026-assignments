# Solution notes: Group anagrams

## Approach

Use a `HashMap<String, Vec<String>>` where the key is an anagram signature and the value is the list of words that share that signature.
For each word:
Convert it to lowercase to perform case-insensitive comparison.
Collect its characters into a vector.
Sort the characters.
Convert the sorted characters back into a `String`; this becomes the signature.
Insert the original word into the vector associated with that signature.

## Edge cases handled
Empty input returns an empty vector.
Words with different casing are grouped together because signatures are generated from lowercase characters.
Original casing is preserved in the output because the original words are stored in each group.

## Anything special

`sort_unstable()` is used to sort the characters of each word and create a canonical anagram signature.
`entry()` provides a convenient way to access a key in the `HashMap` whether it already exists or not, avoiding a separate lookup.
`or_insert_with(Vec::new)` creates and inserts a new empty `Vec<String>` only when the signature is not already present in the map. If the key exists, it returns a mutable reference to the existing vector.
