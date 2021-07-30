### Exercises 1.1 (1)
> Read the input one line at a time and then write the lines out in reverse order, so that the last input line is printed first, then the second last input line, and so on.

Implementation in pseudocode:
```
; The domain of this function is NULL, because this function doesn't take input.
; Also, the Range of this function is StackADT, because it's returning Stack.          
{String} -> {StackADT}                           
FUNCTION read-input(text-file:String)
  WHILE text-file AS line WHERE line IS ¬EOF DO           
    StackADT.Push(line)                                    ; Push/Add {line} to Stack
  END LOOP.
END FUNCTION.

PROCEDURE write-input(stack-input:StackADT)
  WHILE stack-input WHERE IS ¬NULL DO
    element ← stack-input.Pop()                            ; Pop {stack-input} and STORE to {element}
    WRITE element                                          ; WRITE element to output
  END LOOP.
END PROCEDURE.
```
**Note:** \
This pseudocode is **not standard**. This pseudocode is created by myself. \
That pseudocode style, are influenced from Mathematics, Textbook pseudocode, Pascal, Python, Assembly, SQL, VBA & Java

My Implementation: [C++](https://gist.github.com/afifabroory/e03c2179550c72828ea40bd38d909e0e)


---

### Exercuses 1.1 (2)
> Read the first 50 lines of input and then write them out in reverse order. Read the next 50 lines and then write them out in reverse order. Do this until there are no more lines left to read, at which point any remaining lines should be output in reverse order.
In this pseudocode,
```
PROCEDURE write-fifty-input()
  WHILE text-file AS line WHERE IS ¬EOF DO
```
