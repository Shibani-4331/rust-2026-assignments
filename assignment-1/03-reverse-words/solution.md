# Solution notes: Reverse the word order

## Approach

Split the sentence into whitespace-separated words,iterate them in reverse order, append them to new String

## Edge cases handled

- Empty input returns an empty String.
- Whitespace-only input returns an empty String.
- Multiple spaces between words are handled correctly by split_whitespace().

## Anything special

- Uses split_whitespace().rev() to iterate over words in reverse order.
- Builds the result manually using String::push and String::push_str.
