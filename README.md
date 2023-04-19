# Lab-7_202001050

## Section A
|**Tester Action and Input Data**|**Expected Outcome**|
|--------------------------------|--------------------|
|*Equivalence Partioning*||
|(5, 6, 2000)|(4, 6, 2000)|
|(1, 1, 1900)|Invalid Date|
|(31, 12, 2015)|(30, 12, 2015)|
|(0, 6, 2000)|Invalid Input|
|(32, 6, 2000)|Invalid Input|
|(5, 13, 2000)|Invalid Input|
|(5, 0, 2000)|Invalid Input|
|(5, 6, 1899)|Invalid Input|
|(5, 6, 2016)|Invalid Input|
|*Boundary Value Analysis*||
|(1, 1, 1900)|Invalid Date|
|(1, 1, 1901)|(31, 12, 1900)|
|(31, 12, 1900)|Invalid Date|
|(31, 12, 1901)|(30, 12, 1901)|
|(1, 1, 2015)|(31, 12, 2014)|
|(31, 12, 2014)|(30, 12, 2014)|
|(31, 12, 2015)|Invalid Date|
|(0, 6, 2000)|Invalid Input|
|(32, 6, 2000)|Invalid Input|


## P1
|**Tester Action and Input Data**|**Expected Outcome**|
|--------------------------------|--------------------|
|*Equivalence Partioning*||
|a = 1, b = 2, c = 3|Yes|
|a = -1, b = 2, c = 3|An Error message|
|a = 101, b = 2, c = 3|An Error message|
|a = 50, b = 101, c = 3|An Error message|
|a = 50, b = -1, c = 3|An Error message|
|a = 50, b = 2, c = -1|An Error message|
|*Boundary Value Analysis*||
|a = 0, b = 1, c = 2|Yes|
|a = 100, b = 99, c = 98|Yes|
|a = -1, b = 1, c = 2|An Error message|
|a = 101, b = 99, c = 98|An Error message|
|a = 50, b = 0, c = 2|An Error message|
|a = 50, b = 99, c = 100|An Error message|


## P2
|**Tester Action and Input Data**|**Expected Outcome**|
|--------------------------------|--------------------|
|*Equivalence Partioning*||
|a = 10, b = 20, c = 30|The output of the program with the given input|
|a = -10, b = 20, c = 30|An error message|
|a = 110, b = 20, c = 30|An error message|
|a = 50, b = -20, c = 30|An error message|
|a = 50, b = 20, c = -30|An error message|
|*Boundary Value Analysis*||
|a = 0, b = 1, c = 2| The output of the program with the given input|
|a = 100, b = 99, c = 98| The output of the program with the given input|
|a = -1, b = 1, c = 2|An error message|
|a = 101, b = 99, c = 98|An error message|
|a = 50, b = 0, c = 2|An error message|
|a = 50, b = 99, c = 100|An error message|

## P3
|**Tester Action and Input Data**|**Expected Outcome**|
|--------------------------------|--------------------|
|*Equivalence Partioning*||
|v is present in a|Index of v|
|v is not present in a|-1|
|*Boundary Value Analysis*||
|Empty array a|-1|
|v is present at the first index of a|0|
|v is present at the last index of a length of a|-1|
|v is not present in a|-1|

## P4
|**Tester Action and Input Data**|**Expected Outcome**|
|--------------------------------|--------------------|
|*Equivalence Partioning*||
|Invalid triangle (a+b<=c)|INVALID|
|Valid equilateral triangle (a=b=c)|EQUILATERAL|
|Valid isosceles triangle (a=b<c)|ISOSCELES|
|Valid scalene triangle (a<b<c)|SCALENE|
|*Boundary Value Analysis*||
|Invalid triangle (a+b<=c)|INVALID|
|Invalid triangle (a+c<b)|INVALID|
|Invalid triangle (b+c<a)|INVALID|
|Valid equilateral triangle (a=b=c)|EQUILATERAL|
|Valid isosceles triangle (a=b<c)|ISOSCELES|
|Valid isosceles triangle (a=c<b)|ISOSCELES|
|Valid isosceles triangle (b=c<a)|ISOSCELES|
|Valid scalene triangle (a<b<c)|SCALENE|

## P5
|**Tester Action and Input Data**|**Expected Outcome**|
|--------------------------------|--------------------|
|*Equivalence Partioning*||
|Empty string s1 and s2|True|
|Empty string s1 and non-empty s2|True|
|Non-empty s1 is a prefix of non-empty s2|True|
|Non-empty s1 is not a prefix of s2|False|
|Non-empty s1 is longer than s2|False|
|*Boundary Value Analysis*||
|Empty string s1 and s2|True|
|Empty string s1 and non-empty s2|True|
|Non-empty s1 is not a prefix of s2|False|
|Non-empty s1 is longer than s2|False|

# Section B:

**1. Control flow diagram**<br>
![control-flow-diagram drawio](https://user-images.githubusercontent.com/84441910/231426230-4f73e587-ef87-4d39-83df-3722a17df30d.png)

**2. Test sets**<br>

Statement coverage test sets: To achieve statement coverage, we need to make sure that every statement in the code is executed at least once.<br>
Test 1: p = empty vector<br>
Test 2: p = vector with one point<br>
Test 3: p = vector with two points with the same y component<br>
Test 4: p = vector with two points with different y components<br>
Test 5: p = vector with three or more points with different y components<br>
Test 6: p = vector with three or more points with the same y component<br>


Branch coverage test sets: To achieve branch coverage, we need to make sure that every possible branch in the code is taken at least once<br>
Test 1: p = empty vector<br>
Test 2: p = vector with one point<br>
Test 3: p = vector with two points with the same y component<br>
Test 4: p = vector with two points with different y components<br>
Test 5: p = vector with three or more points with different y components, and none of them have the same x component<br>
Test 6: p = vector with three or more points with the same y component, and some of them have the same x component<br>
Test 7: p = vector with three or more points with the same y component, and all of them have the same x component<br>


Basic condition coverage test sets: To achieve basic condition coverage, we need to make sure that every basic condition in the code (i.e., every Boolean subexpression) is evaluated as both true and false at least once<br>
Test 1: p = empty vector<br>
Test 2: p = vector with one point<br>
Test 3: p = vector with two points with the same y component, and the first point has a smaller x component<br>
Test 4: p = vector with two points with the same y component, and the second point has a smaller x component<br>
Test 5: p = vector with two points with different y components<br>
Test 6: p = vector with three or more points with different y components, and none of them have the same x component<br>
Test 7: p = vector with three or more points with the same y component, and some of them have the same x component<br>
Test 8: p = vector with three or more points with the same y component, and all of them have the same x component.<br>
