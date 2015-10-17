---
layout: post
title: Intro to Javascript Regexes
---
{{in progress}}

Regular Expressions (Regex for short) are a powerful technique for searching text.  They allow you to concisely describe a pattern you want to match in a give string.  However, they can also be a little intimidating, as to the beginner they look like a incomprehensible series of symbols (for the ultimate confusing regex example, check out this one for validating email addresses http://www.ex-parrot.com/pdw/Mail-RFC822-Address.html).  In this post, we're going to build up the basics of constructing regexes with a few simple exercises that'll get you regexing in no time.  (Note: this article will be using the syntax of Javascript regexes; there are occasionally small differences between different languages' implementations.)

Basics

The simplest kind of regex is simply a string of characters to match exactly.
For example /cat/ is only going to match the string 'cat'.
To add a bit of flexibility, we can surround some characters in brackets.  This would 
indicate a match with any one of the characters within the brackets.  Example: /[cb]at/ will match both 'cat' and 'bat'.

What about repeated characters? for this we can use a *.  This will match the preceding element 0 or more times.  /c*at/ will match 'cat', 'cccat', and 'at'.   + has a similar function, except the element must occur at least once (so /c+at/ would not match 'at').  Let's try a few exercises.

1.  write a regex that will match either 'meat' or 'meet'. 

2. write a regex to match at least one 's', followed by either a '5' or a '6', followed by any number of 't's.

3.

4. What does this regex do? /[mcb][ia]*n/







Answers:
1.

2.

3

Resources:
This site is great for checking that your regexes do what you expect: https://regex101.com/