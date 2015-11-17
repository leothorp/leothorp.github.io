
Newcomers to Javascript are often confused by the presence of two comparison operators: '== and ==='.  At first glance, they appear to do
the same thing: checking whether two values (or expressions) are equal.
For example, 2 == 3 returns false, as does 2 === 3.  
Likewise, 'yes' == 'yes' and 'yes' === 'yes' both return true.
But what about something like 12 == '12'?  To the left of the == is a number, but to the right is a string.  In one sense, these values are clearly different to the computer because they have different types.  But in another sense, they both encode the same idea: the number 12. 
Perhaps there are situations where we want to choose in which sense we are comparing two items.  It turns out that the two comparison operators give us this choice.  == is the less strict of the two.
When presented with two values of different types, Javascript will attempt to coerce them to be the same type before making a comparison. 
So in the case of 2 == '2', the '2' string will be converted to a number and then compared to 2, which will return true.  This can have unexpected results: for example, true == 1 will return true, because 1 is interpreted as true when coerced into a Boolean.  For this reason, it's usually better to use ===.  === is more strict, and will attempt no type coercion before making the comparison.  2 === '2' will return false.  As a final exercise, try to work out the value of this boolean expression in Javascript:

((true == 1) && (3 - 2 === 1)) && ((7 == '7') || (0 === false));  