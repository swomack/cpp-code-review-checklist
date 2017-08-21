# cpp-code-review-checklist
C++ code review checklist. 

## 1. The Rule of The Three

If a class implements one of the following 3 methods, then the class should implement all 3 of them - 

* Destructor 
* Copy constructor
* Copy assignment operator

**More:** http://www.geeksforgeeks.org/rule-of-three-in-cpp/

## 2. Do not use #define unless you have to

Prefers `inline` for functions, `const` for variables and 'enum' for alias. For string, `const string` or `const char * const` instead of `#define`. 

**More:** http://voidsid.blogspot.com/2007/04/prefer-const-and-inline-to-define.html

## 3. Iteration over STL containers 

For generic code, use range based `for loop` instead of the classical for loop. For all other case, refrain yourself from using classical `for loop`. Instead use - 

```
for(auto& element : elements)
```

**More:** https://stackoverflow.com/questions/36992260/comparing-different-types-of-c-for-loops

## 4. Try to use `const` member functions

All the member functions should be declared as `const` if the function dont modify any value of the object. Otherwise, it will be tough to work with `const reference to object / const object / const pointer to object` (function parameter for most of the case) as non-const member functions cant be called with `const reference to object / const object / const pointer to object`.

**More:** https://turbofuture.com/misc/C-Const-member-function-explained
**Example:** https://github.com/swomack/cpp-tricks/blob/master/Const%20Member%20Function/Const%20Member%20Function/Const%20Member%20Function/Source.cpp


