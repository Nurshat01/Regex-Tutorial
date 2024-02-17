# Title (Regex Tutorial -> Matching an Email)


Matching an email address with a regular expression (regex) is a common task in programming. Email addresses have a specific format, typically consisting of a local part, an @ symbol, and a domain part. To match this format, you can use a regex pattern that checks for the presence of these components in the input string. For example, a simple regex pattern for matching email addresses could be ^\w+@[a-zA-Z_]+?\.[a-zA-Z]{2,3}$. This pattern checks for one or more word characters (\w+) at the beginning of the string (^), followed by an @ symbol, then one or more word characters for the domain name, a period (\.), and finally, two to three alphabetical characters for the top-level domain (TLD).

## Summary

I will be describing a regular expression that matches email addresses. The regex pattern is ^\w+@[a-zA-Z_]+?\.[a-zA-Z]{2,3}$. This pattern checks for the format of an email address, ensuring it has a local part, an @ symbol, and a domain part with a valid domain name and top-level domain (TLD).
## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Resources](#Resources)


## Regex Components
The regex pattern for matching email addresses ^\w+@[a-zA-Z_]+?\.[a-zA-Z]{2,3}$ can be broken down into several components: Below Details

1. ^: Anchors the match at the beginning of the string.
2. \w+: Matches one or more word characters (letters, digits, or underscores). This is the local part of the email address before the @ symbol.
3. @: Matches the @ symbol.
4. [a-zA-Z_]+?: Matches one or more lowercase or uppercase letters or underscores. This is the domain name part of the email address.
5. \.: Matches a literal period (dot). It separates the domain name from the top-level domain.
6. [a-zA-Z]{2,3}: Matches two or three lowercase or uppercase letters. This is the top-level
7. $: Anchors the match at the end of the string.

Together, these components define a pattern that matches email addresses with the format local-part-@-domain.tld, where the local part can contain letters, digits, or underscores, and the domain part consists of letters (uppercase or lowercase) and possibly underscores. Below Details

### Anchors

Anchors in regular expressions are used to specify the position in the text where a match must occur. There are two main anchors: Below Details
1. ^ (caret): Anchors the match at the beginning of the line or string. It asserts that the following regex pattern must appear at the start of the text.
2. $ (dollar sign): Anchors the match at the end of the line or string. It asserts that the preceding regex pattern must appear at the end of the text.
3. Anchors are useful for ensuring that a regex pattern matches the entire line or string, rather than just a portion of it.

### Quantifiers
Quantifiers in regular expressions specify how many times a particular element or group in the regex pattern can repeat. They allow you to match patterns of varying lengths. Some common quantifiers include: Below Details

1. ( * (asterisk): Matches zero or more occurrences of the preceding element. For example, a* matches zero or more 'a' characters.
2. ( + (plus): Matches one or more occurrences of the preceding element. For example, a+ matches one or more 'a' characters.
3. ? (question mark): Matches zero or one occurrence of the preceding element. For example, a? matches zero or one 'a' character.
4. {n}: Matches exactly n occurrences of the preceding element. For example, a{3} matches exactly three 'a' characters.
5. {n,}: Matches n or more occurrences of the preceding element. For example, a{2,} matches two or more 'a' characters.
6. {n,m}: Matches between n and m occurrences of the preceding element. For example, a{2,4} matches between two and four 'a' characters.
7. Quantifiers can be used to make regex patterns more flexible and to match varying lengths of text.

### OR Operator

The OR operator in regular expressions allows you to specify alternatives for a pattern. It is represented by the vertical bar | and is used to match any one of a set of alternatives. Example Below.
1. the pattern cat -->  | <-- dog will match either "cat" or "dog" in a text. If the text contains "cat" or "dog", the pattern will find a match.
2. JavaScript Below code example
```
const pattern = /cat|dog/;
const text = 'I have a cat and a dog.';

const matches = text.match(pattern);
console.log(matches);  
// Output: ['cat', 'dog']
```

### Character Classes
Matching an email address using a regular expression involves validating the format of the email address. Email addresses typically consist of two parts: the local part before the "@" symbol and the domain part after the "@" symbol. Here's a basic example of a regular expression pattern that matches most email addresses: Detail Below
1. ^[a-zA-Z0-9_.+-]+@[a-zA-Z0-9-]+\.[a-zA-Z0-9-.]+$

### Flags
In regular expressions, flags are optional parameters that modify the behavior of the regex pattern. They are placed after the closing delimiter of the regex and are usually represented by a single letter. Here are some common flags: Detail Below.
1. i (ignore case): This flag makes the regex case-insensitive, allowing it to match both uppercase and lowercase letters.
2. g (global): This flag allows the regex to match all occurrences of the pattern in a string, not just the first one.
3. m (multiline): This flag changes the behavior of the ^ and $ anchors to match the start and end of each line within a multi-line string, instead of just the start and end of the entire string.
4. s (dotall): This flag makes the . metacharacter match any character, including newline characters (\n), which it normally does not match.
5. u (unicode): This flag enables full Unicode support for the regex, including proper handling of Unicode characters and properties.
6. y (sticky): This flag requires the match to start at the current position in the string indicated by the lastIndex property of the regex object.
7. These flags can be combined, such as /pattern/gi to perform a global, case-insensitive search. Each flag has its own specific use case and can be quite powerful when used appropriately.

### Grouping and Capturing
In regular expressions, grouping is used to treat multiple characters as a single unit. This is often used in conjunction with quantifiers to specify how many times a group can occur.
1. To create a group,use parentheses ( ).
2. For example, in the regex /(\w+)@(\w+)\.com/, there are two groups: (\w+) which captures the username part of the email, and (\w+) which captures the domain name part before ".com".
3. Capturing groups not only allow user to extract parts of a match for further processing but also enable user to reference them later in the regex or in the replacement string. They are numbered based on the order of their opening parentheses from left to right, starting from 1.
4. a simple example an email matching regex Below:
```
* R egex: /(\w+)@(\w+)\.com/
* Sample Text: "nur.test@emial.com"
* Matches: Group 1: "nur.test"  Group 2: "emial"
```

### Resources
1. https://coding-boot-camp.github.io/full-stack/computer-science/regex-tutorial
2. https://gist.github.com/nicolewallace09/e4dc8aca65e7652501bdb8470df45c77
3. https://www.youtube.com/watch?v=GE-0K0izHVE
4. https://www.tutorialspoint.com/checking-for-valid-email-address-using-regular-expressions-in-java