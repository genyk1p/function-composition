# function-composition
Сomposition of functions
Let's say you have separate functions that ultimately calculate the discount. As a result, we will get the result, but this chain is not entirely convenient. 
What if there is a lot of action? You can run it like this:
const discount = normalizePrice(divide100(multiply20(200)));
But with an increase in the number of functions, this will turn into an unreadable hell. The challenge is to write a compose function that takes all of these
functions and does the same. That is, to organize the composition of functions. There can be any number of functions and they can take only one initial argument.

Second task. Write a composeWithArgs composition function that takes as many arguments as you like at the beginning. Example:

const add1 = function(a){return a + 1}
const addAll3 = function(a,b,c){return a + b + c}
composeWithArgs(add1,addAll3)(1,2,3)  => return 7
