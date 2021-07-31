### Exercises 1.1 (4)
> Read the input one line at a time and write each line to the output if it is not a duplicate of some previous input line. Take special care so that a file with a lot of duplicate lines does not use more memory than what is required for the number of unique lines. 

In this problem, I think the most suit ADT is Set. Because we need to store a distinct (unique) line to a container and also store in ordered.
```
PROCEDURE read-input(inputLine) DO
  setLine AS SetADT                     ; Declare setLine variable AS SetADT
  WHILE inputLine NOT EOF DO
    setLine.Insert(inputLine)           ; Store each line of inputLine while it's not EOF.
  END LOOP.
END PROCEDURE.

PROCEDURE write-input(inputLine) DO
  WHILE inputLine NOT END DO
    WRITE inputLine                     ; Print inputLine
  END LOOP.
END PROCEDURE.
```
[C++](https://gist.github.com/afifabroory/47008ed10ea84361d5b3f064bd9b2863) Implementation
