## How you found the tests with different results?
I used `bash.script.sh` in terminal to check the outputs of every tests, and edited the contents of script.sh, and made it show the name of each file.

## Provide a link to the test-file with different-results.
https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/148.md

https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/501.md

## For each test:
* Describe which implementation is correct.

In both tests, the provided implementation was the correct one. 

* expected outputs for: 

*test-file148*: 
[] (empty)

*test-file501*: 
[foo%5Cbar] 


*provided implementation*


![provided-test-file148](https://user-images.githubusercontent.com/103146938/172986660-3748f945-5e0b-489e-abf1-4c11f6aec171.png)
![provided-test-501](https://user-images.githubusercontent.com/103146938/173125687-d22a6e0e-c660-43c6-9dd7-9ad59b11b67f.png)

*My own implementation*: 

test-file148: index out of bounds error
![my-own-test-file148](https://user-images.githubusercontent.com/103146938/172986741-3250a708-bab5-449c-a9a6-208953be1d49.png)
test-file501: infinite loop 
![my-own-test-file501](https://user-images.githubusercontent.com/103146938/173123873-cea2b5cc-0030-4769-bed4-432048a66557.png)


* Describe the bug.

*test-file148*:

I did not handle the case when neither the parentheses nor the bracket were present in the file. 
In this situation, although I considered the case when the open parenthesis was not present, I hyphothesized the brackets existed. 
Thus, I had an index out of bounds error. I need to include the case when none of the components of each pair of the brckets or the parentheses exist. 
![incorrect-handle1](https://user-images.githubusercontent.com/103146938/172040462-75347547-4bf7-4c81-826a-554bbecea267.png)


*test-file501*: 

The bug was out of the same block of code, due to my lack of consideration of the situation that none of the signature would exist, but because of a different mechanism. Because the `currentIndex` was indeed less than `markdown.length`, the program was in an infinite loop without executing.
![incorrect-handle2](https://user-images.githubusercontent.com/103146938/172040686-d6341368-050c-4feb-a5ee-c74a79dc1263.png)
