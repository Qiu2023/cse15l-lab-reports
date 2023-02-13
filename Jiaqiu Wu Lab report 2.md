## Jiaqiu Wu Lab report2
# Servers and Bugs

### Part1
The code for my StringServer.java is below:
![Image](fig4.png)

The first screenshot of using `/add-messages`:
![image](fig5.png)
- The handleRequest() method is called.
- The relevant argument to this handleRequest() method is url: "http://localhost:4000/add-message?s=Hello",
and the value of relevent field of the class is result: "".
- Changed values of relevant fields of the class are url.getPath():/add-message, parameters:["s", "Hello"],
and result:"Hello\n".
I learned how to use server.java to create a web server with some specific functions.
