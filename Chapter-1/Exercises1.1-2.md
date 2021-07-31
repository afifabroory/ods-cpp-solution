### Exercises 1.1 (2)
> Read the first 50 lines of input and then write them out in reverse order. Read the next 50 lines and then write them out in reverse order. Do this until there are no more lines left to read, at which point any remaining lines should be output in reverse order. 
```
{I_FILE} -> {void}
PROCEDURE read-fifty-input(ByRef text-file:I_FILE)
  
  counter ← 0
  DECLARE my-stack AS StackADT
  
  WHILE text-file AS line WHERE IS ¬EOF DO
    IF counter = 50 THEN DO
      CALL write-input(my-stack)                 ; Call procedure write-input from Exercises 1.1 (1) pseudocode.
                                                 ; write-input argument are pass by reference/address, which is
                                                 ; it will remove all element in Stack, by Pop() operation.
      my-stack.Push(line)
      counter ← 0
    ELSE IF
      my-stack.Push(line)                        ; Push line-by-line to stack.
      counter ← counter + 1
    END IF.
  END LOOP.
  
  IF my-stack IS ¬EMPTY THEN DO                  ; Write stack at remaining lines.
    CALL write-input(my-stack)
  END IF
  
 END PROCEDURE.
```
My implementation: [C++](https://gist.github.com/afifabroory/e4be703c1240a2df186601420ca86dfe)
