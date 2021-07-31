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