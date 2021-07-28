### Exercises 1.1 (1)
> Read the input one line at a time and then write the lines out in reverse order, so that the last input line is printed first, then the second last input line, and so on.
```
; The domain of this function is NULL, because this function doesn't take input.
; Also, the Range of this function is StackADT, because it's returning Stack.          
{String} -> {StackADT}                           
FUNCTION read-input(text-file:String, n:Integer ←	0)       ; Second parameter default value are 0. And store it's as {n} 
  WHILE text-file AS line WHERE line IS ¬EOF  DO           
    StackADT.Push(line)                                    ; Push/Add {line} to Stack

PROCEDURE write-input(stack-input:StackADT)
  WHILE stack-input WHERE IS ¬NULL DO
    element ←	stack-input.pop()                            ; Pop {stack-input} and STORE to {element}
    WRITE element                                           ; WRITE element to output
```
Note: \ 
This pseudocode are **not standard**. This pseudocode are created by myself. 
And this pseudocode style are influenced from Mathematics, Textbook pseudocode, Pascal, Python, Assembly, SQL & Java
### Exercuses 1.1 (2)
> Read the first 50 lines of input and then write them out in reverse order. Read the next 50 lines and then write them out in reverse order. Do this until there are no more lines left to read, at which point any remaining lines should be output in reverse order.
In this pseudocode,
```
PROCEDURE write-fifty-input()
  WHILE text-file AS line WHERE IS ¬EOF DO
```
