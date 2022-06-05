## How you found the tests with different results?
I found the tests by manually trying the test files out in terminal, and just happened to find them with different results in two implementations.

## Provide a link to the test-file with different-results.
https://github.com/nidhidhamnani/markdown-parser/blob/main/test-file7.md
https://github.com/nidhidhamnani/markdown-parser/blob/main/test-parens-inside-link.md

## For each test:
* Describe which implementation is correct.

In both tests, the provided implementation was the correct one. 

* expected outputs for: 

*test-parens-inside-link*: 
[something.com(), something.com((())), something.com, boring.com]

*test-file7*: 
[] (empty)

*provided implementation*

![provided-test-file7](https://user-images.githubusercontent.com/103146938/172039817-20659c30-cc48-4192-bfda-076bcd3bee9f.png)
![provided-test-parens-inside-link](https://user-images.githubusercontent.com/103146938/172039707-852a7a86-32d4-4d91-915d-17ea7bd2829d.png)

*My own implementation*: 

test-file7: index out of bounds error
![my-own-test-file7](https://user-images.githubusercontent.com/103146938/172039847-ebc7e294-a333-4fec-b111-ccc9b860969d.png)
parens-inside-link: infinite loop
![my-own-test-](https://user-images.githubusercontent.com/103146938/172039931-5d49ad3f-2608-4455-85a3-5a9ff00eafe0.png)

* Describe the bug.

*test-file7*:

I did not handle the case when the close parenthesis and the open bracket were right next to each other and there was nothing else in the file. 
In this situation, although I considered the case when the open parenthesis was not present, I regarded the close paren did not exist as well. 
Thus, I had an infinite loop. I need to include the case when only one component of each pair of the brckets or the parentheses exist. 
![incorrect-handle1](https://user-images.githubusercontent.com/103146938/172040462-75347547-4bf7-4c81-826a-554bbecea267.png)


*test-parens-inside-link*: 

I ingnored the situation when there could be multiple parenthesis or bracket in the same line. I only handle a single case when open paren did 
not exist, but not the one that a single paren could be outside of the range where the program had checked, thus leading to the index out of bounds error. 
![incorrect-handle2](https://user-images.githubusercontent.com/103146938/172040686-d6341368-050c-4feb-a5ee-c74a79dc1263.png)
