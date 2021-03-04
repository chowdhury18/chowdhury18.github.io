# Clean Code (Robert C. Martin)

## Chapter-3 (Functions)
---
### Function Arguments
- Number of arguments of a function:
    - zero (niladic)
    - one (monadic)
    - two (dyadic)
    - three (triadic)
    - more than three (polydic)
- Two common reason to pass single argument into a function:
    - asking a question about the argument
    ```java
    boolean fileExists("myFile"){}
    ```
    - Transforming the argument into something else
     ```java
    InputStream fileOpen("myFile"){}
    ```
    - Another less common but useful form for a single function argument is **event**. One input argument but no output argument.
    ```java
    void passwordAttemptFailedNTimes(int attempts)
    ```
- Passing **boolean** as a function argument is a truly terrible practice.
    - Invalide the common idea of a function (one function does only one thing). e.g., The function does one thing if the flag is true and another thing if the flag is false.
- If a function needs three or more argument, a better practice should be to wrap the arguments into a class of their own.
    ```java
    Circle makeCircle(double x, double y, double radius)
    Circle makeCircle(Point point, double radius)
    ```
