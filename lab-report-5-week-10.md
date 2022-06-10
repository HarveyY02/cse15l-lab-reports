## How you found the tests with different results?
I found the tests by manually trying the test files out in terminal, and just happened to find them with different results in two implementations.

## Provide a link to the test-file with different-results.
https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/148.md

https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/.md

## For each test:
* Describe which implementation is correct.

In both tests, the provided implementation was the correct one. 

* expected outputs for: 

*test-file148*: 
[] (empty)

*test-file649*: 
[] (empty)

*provided implementation*


![provided-test-file148](https://user-images.githubusercontent.com/103146938/172986660-3748f945-5e0b-489e-abf1-4c11f6aec171.png)
![provided-test-649](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/649.md)

*My own implementation*: 

test-file7: index out of bounds error
![my-own-test-file148](https://user-images.githubusercontent.com/103146938/172986741-3250a708-bab5-449c-a9a6-208953be1d49.png)
parens-inside-link: 
![my-own-test-]()

* Describe the bug.

*test-file148*:

I did not handle the case when neither the parentheses nor the bracket were present in the file. 
In this situation, although I considered the case when the open parenthesis was not present, I hyphothesized the brackets existed. 
Thus, I had an index out of bounds error. I need to include the case when none of the components of each pair of the brckets or the parentheses exist. 
![incorrect-handle1](https://user-images.githubusercontent.com/103146938/172040462-75347547-4bf7-4c81-826a-554bbecea267.png)


*test-parens-inside-link*: 

I ingnored the situation when there could be multiple parenthesis or bracket in the same line. I only handle a single case when open paren did 
not exist, but not the one that a single paren could be outside of the range where the program had checked, thus leading to the index out of bounds error. 
![incorrect-handle2](https://user-images.githubusercontent.com/103146938/172040686-d6341368-050c-4feb-a5ee-c74a79dc1263.png)
