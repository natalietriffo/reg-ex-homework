# Match HEX values and Regular Expression 
The information below is a breakdown of how specific regular expression works. The specific regular expression is used to match a HEX value. In each section of this file there will be explanations to every element of the regular expression and how it operates.

## Summary

For this project, I will be examining the following regular expressions used to match HEX values:

/^#?([a-f0-9]{6}|[a-f0-9]{3})$/

Below is comprehensive explanation for the anchors, quantifiers, grouping and capturing, bracket expressions, and OR Operator used in this regular expression.
## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [The OR Operator](#the-or-operator)

## Regex Components

### Anchors

Anchors alone do not pair with any regular expression. They are used to define where some text may be located. For example, a person might be looking for segment, however only if it is at the start or end of a string, not including when the expression could be used within the subject matter.

Starting example: ^This means that the string must start with This
Ending example: end$ means that the string must end with end.

The ^ is an anchor that specifies that the start of the string must coordinate with #. The # is used to differentiate a decimal and a hexadecimal value.

Anchor:$
Code: $/

Just like the ^ anchor, $ is used to make sure the string fully coordinates with the pattern. The difference is, $ applies the pattern at the end of the string.

In this particular situation the ending section of the string has to coordinate with the three or six pattern recognized before the the $ anchor.

### Quantifiers
? is equal to a boolean value of 0 or 1. Usally, this makes the following optional. In the string this means the # is not essential. In our regex, the quantifier ? suggests that the symbols # preceding the quantifier ? is elective. It's optional for # to appear at the beginning of the expression.For example,The user could operate with A4F and/or #A4F without issue.


Quantifier: {}
Code: [a-f0-9]{6} Code: [a-f0-9]{3}

The Quantier above deminstrates how many times the patten in the code has a match, this is called a Bracket Expression. The number displayed within the brackets means we are searching for specifically that amount of characters in that segment its correlated to.

Example: 2{5} shows us that that two must be repeated five times over again. Therefor, the matching string must be 22222.

In our regex example,{6} explains that there are six occasions of the string in the following square brackets expression. Meaning, that the quantifier will permit 6 symbols in the string with letters a-f and/or numbers 1-9. {3}explains that there are six occasions of the string in the following square brackets expression. Meaning, that the quantifier will permit 6 symbols in the string with letters a-f and/or numbers 1-9.

### Grouping and Constructs 
Code: ([a-f0-9]{6}|[a-f0-9]{3})
 The () groups the regular expression between them. This creates an expression that holds multiple carachters, but is viewed as a single unit. This data can be understood in the form of an array. Values can be veiwed using an index on the result of the match.

Example: (cat){4} matched catcatcat. The value of 'cat' has to be repeated four times, specified in the quantifier.

In this example, the grouped expression is a bracket expression. More information can be seen in the next section below. All in all, the end string anchor $ is applied to this grouping.

### Bracket Expressions 
Code: [a-f0-9]
Bracket Expressions is a regex that is used to match a particular pattern of characters. The characters can be numeric,alphabetic, special characters, ect. However, they must appear with brackets. When a range of chaaracter or symbols are being described, usally a gyphen is used to set them. For example, [1-9]. 

Example:[a-n 1-7] shows that the string contains at least one letter between a and n or 1-7

In our example, the bracket [] expression shows the user that matching a string that contains any lower case character between a-f (becasue of the [a-f]) or any integer between 0-9 (because of the [0-9])

### OR Operator
Code: [a-f0-9]{6}|[a-f0-9]{3}
 The | indicator also known as the OR Operator is a boolean that matches either the expression before or after. A hex code is typically expressed by a sequence of six symbols. Futhermore, sometimes the case is that the 1st and 2nd symbol of each pair in the Code are identical. When this is the case, it can be shown with only three symbols. Appose to the standered six. For example., the color #113355 would show the same color as #135.

Example: 2|6 shows that 2 or 6 or both integers are can be in the string. 262 or 222 or 666 are all okay matching patterns.

In the example above, the match with 3 character string holding lowercase a-f and/or integer 0-9 OR a string with 6 characters holding lowercase a-f and/or integer between 0-9. A matching string has to have 3 or 6 character with the given pattern. Anything other than 3 or 6 symbols won't work.

### Author
My name is Natalie Triffo, I am 21 years old. I am a student as well as a full time bartender. I recently graduated from Oakton community College with my Associates in Business. After graduation, I decided to continue with my academic journey and applied to do the Coding Bootcamp

