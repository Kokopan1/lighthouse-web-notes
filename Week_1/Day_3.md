# Coercion and TruthyFalse

operators
=== compares values and types ie types include strings, numbers ect
== operator before performing a comparison, the operatir will attemp to force the two values to be of the same type if possible, this is <b>type coercion<b>
so == only compares value and not types, it tries to do type coercion
example 23 = "23", this will return true by of type coercion ... use triple equal all the time ===



What about not equal?
!== strict, != will force type coercion

Truthy and Falsey
Comparing two values in JavaScript will return either true or false. But there are some situations in JavaScript, especially when using ==, that the correct response will be the opposite of what you might expect.

example 0 == false // will evaluate to true
WHY?
b/c everything has an <b>inherent boolean value<b> referred to as Truthy or False value
Most things are considered truthy except the <b>following<b>

// All of the following are inherently falsey:

False
// False is False. Makes sense, right?

0
// 0 is the only falsey Number

""
// an empty string is falsey

null
// a null, or empty value, is falsey.

undefined
// an object that has not been defined is considered falsey.

NaN
// Not a Number. You'll learn more about NaN as we go on.


So... How Do I Use It?
Truthy values are a fast and easy way to check conditions in our code. For example, maybe we want to save the users name to a String, but only if we don't already have something saved to username.

username = '';

if (!username) {
  username = 'Siobhan';
}
Since we haven't yet saved anything to username, it's an empty String, and therefore returns falsey, which we account for with the bang !username, allowing the rest of our code to run.

The same concept can be applied to Arrays. Invoking the Array.length property will return 0 for an empty Array, which is also a falsey value.

shoppingList = [];

if (!shoppingList.length) {
  shoppingList.push('coconut milk');
}