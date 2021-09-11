# Regular Expression Matching Email Tutorial

A Regular Expression or Reg-Ex is a series of characters that specify a specific search pattern. A Reg-ex sequence can be used with almost any programming language. These expressions are typically used to search string elements for specific information. Other uses consist of validation, parcing/replacing strings, translating data, web scraping, etc. Below is a step by step tutorial explaining a Reg-Ex sequence used to validate or match email. 

## Summary

The pattern below could be used to validate an email address for a user. If a user fills out a form on the application, this pattern can be used to establish a new user email, confirm it is an actual email, and ensure that this email hasn't been used for another account. Regular expressions are small amounts of code but provide a crucial utility to applications.

##### Matching an Email Reg-Ex Pattern: 
``` /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/ ```


## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

### Anchors

Anchors are used to establish the beginning and the end of the Reg-Ex. The ```^``` symbol represents the start of the expression. The application will now search for strings that begin with the pattern following the ```^```. In this case, our expresssion ```^([a-z0-9_\.-]+)``` identifies a series of characters that an email is capable of having.

The end of the pattern is identified with a ```$``` symbol. This signifies how and when a pattern ends. In our case, the ending can only match a top level domain like .com or .net. The numbers enclosed in squigly brackets ```{2,6}``` specify the minimum and maximum length of the string for that specific group. 

### Quantifiers

Quantifiers represent which characters, groups, or character classes must be represented in order for the expression to match the string in question. For example, will the string contain, letters, numbers, or any other symbols? Each block of the string is surrounded with ```()``` and the quantifiers are contained in ```[]```. Our first block, ```^([a-z0-9_\.-]+)``` can be broken down as follows: ```a-z``` searches for any letter as long as its lowercase. If you wanted to look for just capital letters if would be written like this ```A-Z```. ```0-9``` searches for any combination of numbers. ```_\.-``` will search for any of those symbols. The ```+``` sign will search for one or more matching patterns. 

### OR Operator

The ```|``` operator is used to search for more complex sequences. We did not use it in this example. 

### Character Classes

In this example the character class ```\d``` is used following the ```@``` symbol in the email. This expression is requiring that a letter follows the ```@``` symbol to make sure the domain in the email is valid. 

### Flags

An expression is enclosed with a flag ```//``` surrounding the anchors. We can classify flags that change the way we search for a match. In this case, it is not used. 

### Grouping and Capturing

As stated above, a group is enclosed within parentheses ```()```. The first group must match or be captured before the next set in the sequence can be verified. 

### Bracket Expressions

If we return to the original expression, ``` /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/ ``` We can see the brackets enclosing a series of symbols which represent the qualifing parameters of each group. 

### Greedy and Lazy Match

Greedy matches search for as many matches as possible while lazy matches will match the minimum amount required. 

### Boundaries

Boundaries are not used in this example but they add specifics to the pattern search.

### Back-references

Back references are also not used in this example but they require a match between the first capturing group with the following capturing group. 

### Look-ahead and Look-behind

This will require a matching to sequence in a specific order. It is not used in the given example. 

## Author

Written by: Max Fausnight

[Git-hub](https://github.com/fausnightm)


