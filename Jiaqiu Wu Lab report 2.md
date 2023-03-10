## Jiaqiu Wu Lab report2
# Servers and Bugs

### Part1

The code for my StringServer.java is below:

```
import java.io.IOException;
import java.net.URI;

class Handler implements URLHandler {
    
    String result = "";

    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return String.format("Use /add-message?s=... to add sentences");
        } else if (url.getPath().contains("/add-message")) {
            String[] parameters = url.getQuery().split("=");
            if (parameters[0].equals("s")) {
                result += parameters[1];
                result += "\n";
            }
            return String.format(result);
        } else {
    
            return "404 Not Found!";
        }
    }
}

class StringServer {
    public static void main(String[] args) throws IOException {
        if(args.length == 0){
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }

        int port = Integer.parseInt(args[0]);

        Server.start(port, new Handler());
    }
}
```


The first screenshot of using `/add-message?s=Hello`:

![Image](fig5.png)

- The handleRequest() method is called.
- The relevant argument to this handleRequest() method is url: "http://localhost:4000/add-message?s=Hello",
and the value of relevent field of the class is result: "".
- Changed values of relevant fields of the class are url.getPath():/add-message, parameters:["s","Hello"],
and result:"Hello\n".


Thd second screenshot of using `/add-message?s=How are you`:

![Image](fig6.png)

- The handleRequest() method is called.
- The relevant argument to this handleRequest() method is url: "http://localhost:4000/add-message?s=How are you",
and the value of relevent field of the class is result: "Hello\n".
- Changed values of relevant fields of the class are url.getPath():/add-message, parameters:["s","How are you"],
and result:"Hello\nHow are you\n".


### Part2

I choose the bugs from `static int[] reversed` method in ArrayExamples.java.
- A failure-inducing input and its JUnit test:
  ```
  int[] input1 = {1, 2, 3};
    assertArrayEquals(new int[]{3, 2, 1}, ArrayExamples.reversed(input1));
  ```
  
- A input that doesn???t induce a failure and its JUnit test:
  ```
  int[] input1 = {0, 0, 0};
    assertArrayEquals(new int[]{0, 0, 0}, ArrayExamples.reversed(input1));
  ```
  
- The symptom after running the two JUnit tests above in VScode:
  
  For the failure-inducing input:
  
  ![Image](fig7.png)
  
  For the input that doesn???t induce a failure:
  
  ![Image](fig8.png)
  
- Bug fix:
  
  Before:
  ```
  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
  }
  ```
  
  After:
  ```
  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      newArray[arr.length - i - 1]=arr[i] ; 
    }
    return newArray;
  }
  ```
  
`arr` is the parameter to be reversed, so we should return `newArray` which is the reversed copy of `arr`.
And in the for loop, `arr` should give its values to `newArray` in inverse order 
instead of `new Array` giving to `arr`. Thus, it should be written as `newArray[arr.length - i - 1]=arr[i] ;`.


### Part3

I learned how to process different URIs entered by users in the 
handleRequest method to form different response results.
For the web server in this lab report, the string has been appended to retain the user input and form the result.
I also learned how to use Junit for unit testing and modify the source code according to the test results.
