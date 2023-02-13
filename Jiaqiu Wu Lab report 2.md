## Jiaqiu Wu Lab report2
# Servers and Bugs

### Part1
The code for my StringServer.java is below:
![Image](fig4.png)

The first screenshot of using `/add-messages`:
![Image](fig5.png)
- The handleRequest() method is called.
- The relevant argument to this handleRequest() method is url: "http://localhost:4000/add-message?s=Hello",
and the value of relevent field of the class is result: "".
- Changed values of relevant fields of the class are url.getPath():/add-message, parameters:["s", "Hello"],
and result:"Hello\n".\

### Part3
I choose the bugs from `static int[] reversed` method in Array Methods.
- A failure-inducing input and its JUnit test:
  `int[] input1 = {1, 2, 3};
   assertArrayEquals(new int[]{3, 2, 1}, 
   ArrayExamples.reversed(input1));`
- A input that doesn’t induce a failure and its JUnit test
  `int[] input1 = {0, 0, 0};
   assertArrayEquals(new int[]{0, 0, 0},
   ArrayExamples.reversed(input1));`
- The symptom after running the two JUnit tests above in VScode:\
  For the failure-inducing input:
  ![Image](fig7.png)
  For the input that doesn’t induce a failure:
  ![Image]()
  
    
