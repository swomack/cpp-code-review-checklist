# cpp-code-review-checklist
C++ code review checklist. 

## The Rule of The Three

If a class implements one of the following 3 methods, then the class should implement all 3 of them - 

* Destructor 
* Copy constructor
* Copy assignment operator

**More:** http://www.geeksforgeeks.org/rule-of-three-in-cpp/

## Do not use #define unless you have to

Prefers `inline` for functions, `const` for variables and 'enum' for alias. 

**More:** http://voidsid.blogspot.com/2007/04/prefer-const-and-inline-to-define.html
