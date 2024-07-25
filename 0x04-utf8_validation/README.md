Problem Description
The UTF-8 Validation problem involves validating whether a given list of integers represents a valid UTF-8 encoding. UTF-8 is a variable-length character encoding that can represent various characters from different languages and symbols.

To solve the UTF-8 Validation problem, you need to determine whether the sequence of bytes provided follows the rules of valid UTF-8 encoding.

Rules for Valid UTF-8 Encoding
A valid UTF-8 character can be 1 to 4 bytes long.
For a character with N bytes, the first byte starts with N 1s and a 0 (N consecutive "1" bits followed by a "0" bit), while the following N-1 bytes start with "10".
The remaining bytes must all start with the bit pattern "10".
Approach
To solve this problem, you can follow these steps:

Initialize a variable to keep track of the number of bytes remaining for the current character (initially set to 0).
Iterate through each byte in the given sequence of bytes.
If the bytes_to_follow variable is 0, determine the number of bytes for the current character based on the first byte's pattern.
If the bytes_to_follow variable is not 0, check that the current byte starts with the pattern "10".
Update the bytes_to_follow variable accordingly.
After processing all bytes, check if the bytes_to_follow variable is 0. If it is, the sequence is valid; otherwise, it's not.
