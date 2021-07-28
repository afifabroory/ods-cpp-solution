### Exercises 1.1
> Read the input one line at a time and then write the lines out in reverse order, so that the last input line is printed first, then the second last input line, and so on.
```
; The domain of this function is NULL, because this function doesn't take input.
; Also, the Range of this function is StackADT, because it's returning Stack.          
{NULL} -> {StackADT}                           
FUNCTION read-input()
  READ text-file                            ; READ input, then STORE to {text-file-line}
  WHILE text-file AS line IS ¬EOF DO           
    StackADT.Push(line)                     ; Push/Add {line} to Stack
   
{StackADT} -> {NULL}
PROCEDURE write-input(stack-input)
  WHILE stack-input IS ¬NULL DO
    STORE element, stack-input.pop()        ; Pop {stack-input} and STORE to {element}
    WRITE element                           ; WRITE element to output
```
  
