# Regex Tutorial for Matching an Email

### Regex or regular expressions is a tool for processing text that allows a user to search through text for a specific pattern and find matches to the specified string. Regex comes in handy for combing through long lines of text for specific information or to keep information private and encrypted. Regex can be used to set search parameters for all kinds of patterns like URL's, emails, and phone-numbers along with many others. In this Regex tutorial, users will be given a walk-through on how to use regex for matching an email and setting up the correct syntax for users to be able to search for emails. 

## Summary

### A Regex for email is a very useful tool that can go through any body of information and search specifically for any text or code that contains emails by searching for the characters we specified in our regex code. This tutorial will explain step-by-step the process for using regex for emails.

### (Here is a code example of an email Regex) => `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

## Table of Contents

- [Anchors](#anchors)
- [Bracket Expressions](#bracket-expressions)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Character Classes](#character-classes)
- [Character Escapes](#character-escapes)
- [Author](#author)

## Regex Components

### Anchors

### Anchors specify where a string will start and end. The anchor ^ means that a string will begin with whatever follows it. The anchor $ means that a string will end with whatever is before (precedes) it. For example in the following code -- ^hello$ -- the string will start from lowercase "h" and end with lowercase "o". This is known as an exact string match because it is read exactly as written-with lowercase letters. If it was written in capital letters (i.e. -- ^HELLO$ --), the string will start with capital "H" and end with capital "O". 

### Bracket Expressions

### Another way for these anchors to be read is by a range of possible matches which uses square brackets [] to signify what the possible matches are. We put the possible matches we'd like to look for and include in square brackets. Whatever you put in the brackets will be returned no matter the length of that particular string. For example -- [abc123] --- will return anything that contains an "a" or "b" or "c" or "1" or "2" or "3". So these results -- "apple", "ball", "ccc", "2451", "3333", "1678" would fulfil the any possible matches the bracket notation means. This can also be written with a hyphen between letters and numbers so the above example of -- [abc123] -- could be written as -- [a-c] and [1-3] -- and it would mean the same thing. 

### In our previous example -- `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` -- this email regex starts with the anchor ^ which means the string starts after that with the square brackets of any matches from letters "a-z" and numbers "0-9" and ends with the $ anchors with the quantifier {2,6}.

### Quantifiers

### Regex quantifiers set limits to the string that is being searched and it uses curly brackets {} to signify its search limit. There are many types of regex quantifiers: the + quantifier looks for and matches whatever patten one or more times while the {n,x} quantifier looks for and matches patterns an "n" number minimum amount to an "x" number maximum amount, for example {5,10} is specifying the character length to between 5 (as the minimum) and 10 (as the maximum).

### In our example -- `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` -- the regex has the + quantifier which is searching the pattern as many times as it occurs and the {2,6} quantifier is limiting the string to between 2 and 6 characters.  

### Grouping Constructs

### Regex grouping constructs is usually denoted by the parentheses () with everything within a parentheses in their own groups and will be searched for in that particular group. For example -- (123) is one group and (456) is another group. These individual groups will be returned as an exact match unless specified to not do so and so the string will be "123" and "456" and not in any other order. 

### In our example -- `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` -- the string ([a-z0-9_\.-]+) is in a parentheses meaning that it is in its own group and a string that matches only this will be searched while the string ([\da-z\.-]+) and ([a-z\.]{2,6}) are two other groups and will be searched and matched for separate from the other groups but will return an exact match for what is in the parentheses.  

### Character Classes

### A Regex character class defines characters in a string and provides an exact match. The . character class matches any character in the string with the exception of the \n character (newline character). The \d matches any number character in a string (which is the same as [0-9]).

### In our example -- `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` -- the . character class can be seen here ([\da-z\.-]+)\. matching any character in the string while the \d character class can be seen here ([\da-z\.-]+) matching any number character.    

### Character Escapes

### In Regex, character escapes is denoted by the backslash \ and it specifies that a character should be read and matched literally. For example, the curly bracket {} would be read literally as a curly bracket and would be searched for and matched with literally a curly bracket if there was a backslash in front of it \{}. 

### In our example -- `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` -- the character escape can be seen here ([a-z0-9_\. and ([\da-z\. and is escaping the character is it attached to and causing it to be read literally as that character.   

## Author

### Asiya Ahmed is a Seattle-based web developer who loves to make coding simple and easy to follow for coders all around the world! Discover more of her work and visit her GitHub at https://github.com/AsiyahAA
