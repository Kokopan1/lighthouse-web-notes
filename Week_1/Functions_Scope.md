## Function Best Practices - Introduction


#### Growing Functions

Natural ways for functions to be introduced into programs
1. writing similar code multiple tijmes so you take the repeated functionality, name it and put it into a function
2. You havent written a functionality yet so you decide to write one

- Name difficulty indicated how clear a concept of functionality your trying to wrap and code, try to be specific in what naming what the function does

#### Functions and Side Effects

- functions can be divided into those that are called for their
1. side effects
2. return value --> this is more usefull

- functions that create value are easier to combine in new ways than functions that directly perform side effects

- pure function --> specific king of value- producing function that has no side effects but doesnt rely on side effects from other code. It has a pleasant property that, when called with the same arguments, always produces the same value

### Conventions for name
1. avoid generic names like data or run
2. name your functions beginning with action words ie creat user or sendUserData
3. be consistent in naming conventions
4. adapt to existing naming conventions when joining an existing project
5. use camelCase

#### Proper Indentation is Key
- use 2 spaces, not tab