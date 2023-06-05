# Lab Report 5

1.
Whan environment are you using( computer, operating system, web browser, terminal/editor, and so on)? 
Terminal on VS Code 
Detail the symptom you're seeing. Be specific; include both what you're seeing and what you expected to see instead. Screenshots are great, copy-pasted terminal output is also great. Avoid saying “it doesn't work”.
I can't compile and run NumberServer.java.
Detail the failure-inducing input and context. That might mean any or all of the command you're running, a test case, command-line arguments, working directory, even the last few commands you ran. Do your best to provide as much context as you can.

I did not change the given code at all. I think there might be a problem with my working directory...?

2.A response from a TA asking a leading question or suggesting a command to try (To be clear, you are mimicking a TA here.)

Have you tried `cd` into the folder that was just cloned, for example, `cd wavelet`. In the example that was refered to NumberServer.java is not in the current directory since it doesn't exist.

![image](https://github.com/lmillan1/LabReport5/assets/130090548/76a5ac73-64f5-49c3-8a8f-cd55cba41cd4)

3.To fix the issue, you can follow these steps:
Open your terminal in VS Code.
Run the `ls` command to see the files and directories in your current location.
If the output of `ls` does not include the `wavelet` directory, you need to navigate to the correct directory by running `cd wavelet`.
After navigating to the "`wavelet`" directory, use the `ls` command again to confirm that "`NumberServer.java`" is present.
If "`NumberServer.java`" is in the "wavelet" directory, you can compile it by running the command `javac NumberServer.java`.
Once the compilation is successful, you can run the program using the command `java NumberServer`.
Make sure you are in the correct directory that contains the "`NumberServer.java`" file before compiling and running it.

4.
Directory structure:

Copy code
├── LabReport5
│   ├── NumberServer.java
│   └── script.sh
Contents of each file before fixing the bug:

NumberServer.java:

```
import java.util.Scanner;

public class NumberServer {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter a number: ");
        int number = scanner.nextInt();
        scanner.close();

        System.out.println("The square of the number is: " + (number * number));
    }
}
```
```
script.sh:

bash
Copy code
#!/bin/bash

echo "Running the script..."
echo "Executing NumberServer.java..."
java NumberServer
echo "Script execution complete."
```
The bug:

When running the bash script script.sh, instead of providing a valid number as input to NumberServer.java, we mistakenly provide a non-integer value. This will cause the scanner.nextInt() method to throw an exception, resulting in an error message.

Command line to trigger the bug:

Open the terminal in VS Code and navigate to the LabReport5 directory. Then, run the following command:

bash
Copy code
./script.sh
This will execute the bash script and attempt to run `NumberServer.java.`

Description of the bug:

The bug occurs when we run the bash script. It tries to execute NumberServer.java and expects a number as input. However, if we provide a non-integer value (e.g., a string or a floating-point number) instead, the scanner.nextInt() method will throw an exception. This will result in an error message displayed in the terminal.



# Part 2:
During the second half of this quarter, I had the opportunity to dive deeper into GitHub and learn how to navigate and effectively use it for publishing code. I discovered the importance of version control and the benefits of using Git and GitHub for managing code repositories.
By using GitHub, I learned how to create new repositories, initialize them with code, and push my local code to remote repositories. I became familiar with concepts like branches, commits, and pull requests, which helped me collaborate with others on code projects.
