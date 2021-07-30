### Exercises 1.1 (1)
> Read the input one line at a time and then write the lines out in reverse order, so that the last input line is printed first, then the second last input line, and so on.

Implementation in pseudocode:
```
; The domain of this function is NULL, because this function doesn't take input.
; Also, the Range of this function is StackADT, because it's returning Stack.          
{I_FILE} -> {StackADT}                           
FUNCTION read-input(text-file:I_FILE)
  DECLARE my-stack AS StackADT
  WHILE text-file AS line WHERE line IS ¬EOF DO           
    my-stack.Push(line)                                    ; Push/Add {line} to Stack
  END LOOP.
END FUNCTION, RETURN my-stack.

{StackADT} -> {void}
PROCEDURE write-input(ByRef stack-input:StackADT)          ; Pass procedure parameter by address/reference
  WHILE stack-input WHERE IS ¬NULL DO
    element ← stack-input.Top()                            ; Top {stack-input} (return top element) and STORE to {element}
    stack-input.Pop()                                      ; Pop (remove top element)
    WRITE element                                          ; WRITE element to output
  END LOOP.
END PROCEDURE.
```
**Note:** \
This pseudocode is **not standard**. This pseudocode is created by myself. \
The pseudocode style, are influenced from Mathematics, Textbook pseudocode, Pascal, Python, Assembly, SQL, VBA, C/C++ & Java. \
Sorry, if the pseudocode makes you dizzy.

My Implementation: [C++](https://gist.github.com/afifabroory/e03c2179550c72828ea40bd38d909e0e)

---

### Exercuses 1.1 (2)
> Read the first 50 lines of input and then write them out in reverse order. Read the next 50 lines and then write them out in reverse order. Do this until there are no more lines left to read, at which point any remaining lines should be output in reverse order. 
```
{I_FILE} -> {void}
PROCEDURE write-fifty-input(text-file:I_FILE)
  counter ← 0
  DECLARE my-stack AS StackADT
  WHILE text-file AS line WHERE IS ¬EOF DO
    IF counter = 50 then do
      CALL write-input(my-stack)                 ; Call procedure write-input from previous pseudocode.
      counter ← 0
    ELSE IF
      my-stack.Push(line)                        ; Push line-by-line to stack.
      counter ← counter + 1
    END IF.
  END LOOP.
 END PROCEDURE.
```
