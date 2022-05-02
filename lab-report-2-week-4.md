* Screenshot 1:
![Screenshot of the code change 1](https://user-images.githubusercontent.com/103146938/165000252-af5f5b2c-9bb0-4927-be99-7362a3c2a3af.png)
* Link to the failure-inducing input 1:
[Link to the input 1](https://github.com/HarveyY02/markdown-parser/blob/main/lab3Test.md)
* Screenshot for the symptoms:
![Symptom 1](https://user-images.githubusercontent.com/103146938/165000948-8800e229-26df-4b0b-80d6-e857f98332c4.png)
* The original code was only able to give the correct output when the test file was nicely formatted with 2 pairs of links, 
but this test file I created only had one link, and the while loop is thus infinite.

* Screenshot 2:
![Screenshot of the code change 2](https://user-images.githubusercontent.com/103146938/166295359-c86fe7aa-8c13-475a-851d-c14c1abf785e.png)
* Link to the failure-inducing input:
[Link to the input 2](https://github.com/HarveyY02/markdown-parser/blob/main/test-file2.md)
* Screenshot for the symptoms:
![Symptom 2](https://user-images.githubusercontent.com/103146938/166295862-2bc4cbab-2968-40dc-9f98-3c93725d7839.png)
* This test file has only the brackets and not the parentheses, so it originally would print out only empty brackets since.

* Screenshot 3:
![Screenshot of the code change 3]()<img width="535" alt="Screen Shot 2022-05-02 at 10 38 54" src="https://user-images.githubusercontent.com/103146938/166297009-129cca60-d5c0-4d88-bc15-e4d6c5dc67dc.png">

* Link to the failure-inducing input:
[Link to the input 3](https://github.com/HarveyY02/markdown-parser/blob/main/test-file3.md)
* Screenshot for the symptoms:
![Symptom 3](https://user-images.githubusercontent.com/103146938/166296794-7ca127b0-9809-4312-9f61-17dfde40d95e.png)
* The test case had the locations of brackets and parentheses swapped, so the original code would go into an infinite loop and print out nothing.
