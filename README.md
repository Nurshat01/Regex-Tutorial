# Regex Tutorial: Matching an Email

This tutorial explains how to use regular expressions (regex) to match an email address. Email addresses have a specific format, and by using regex, reader can validate whether an input string is a valid email address or not.

## Getting Started

To follow this tutorial, reader should have a basic understanding of regular expressions and their syntax. If reader new to regex, reader can refer to online resources or tutorials to get started.

## Regex Pattern

The regex pattern for matching an email address is:

```regex
^\w+@[a-zA-Z_]+?\.[a-zA-Z]{2,3}$
```
### pattern consists of the following components:
* ^\w+: Matches one or more word characters at the beginning of the string.
* @: Matches the @ symbol.
* [a-zA-Z_]+?: Matches one or more lowercase or uppercase letters or underscores.
* ( . ) : Matches a literal period (dot).
* [a-zA-Z]{2,3}$: Matches two or three lowercase or uppercase letters.

## Usage
```
const regex = /^\w+@[a-zA-Z_]+?\.[a-zA-Z]{2,3}$/;
const email = 'example@email.com';

if (regex.test(email)) {
  console.log('Valid email address');
} else {
  console.log('Invalid email address');
}
```
### Resources
1. https://coding-boot-camp.github.io/full-stack/computer-science/regex-tutorial
2. https://gist.github.com/nicolewallace09/e4dc8aca65e7652501bdb8470df45c77
3. https://www.youtube.com/watch?v=GE-0K0izHVE
4. https://www.tutorialspoint.com/checking-for-valid-email-address-using-regular-expressions-in-java