# Experiment 7: PL/SQL – Variables, Control Structures and Loops

## AIM
To write and execute simple PL/SQL programs using variables, loops, and conditional statements.


## THEORY

PL/SQL, which stands for Procedural Language extensions to the Structured Query Language (SQL). It is a combination of SQL along with the procedural features of programming languages.

**Syntax:**
```sql
DECLARE 
   <declarations section> 
BEGIN 
   <executable command(s)>
EXCEPTION 
   <exception handling> 
END;
```

### Basic Components of PL/SQL Block:
- DECLARE: Section to declare variables and constants.
- BEGIN: The execution section that contains PL/SQL statements.
- EXCEPTION: Handles errors or exceptions that occur in the program.
- END: Marks the end of the PL/SQL block.

# PL/SQL Programs – Steps and Expected Output

## 1. Write a PL/SQL program to find the Greatest of Two Numbers

### Program:
```sql
   DECLARE
    A NUMBER := 10;
    B NUMBER := 20;
BEGIN
    IF A > B THEN
        DBMS_OUTPUT.PUT_LINE('Greatest number is: ' || A);
    ELSE
        DBMS_OUTPUT.PUT_LINE('Greatest number is: ' || B);
    END IF;
END;
/
```

### Steps:
- Declare two numeric variables and initialize them.
- Use an `IF` statement to compare the values.
- Display the greater number using `DBMS_OUTPUT.PUT_LINE`.

**Expected Output:**  
<img width="400" height="240" alt="image" src="https://github.com/user-attachments/assets/39466aea-4f51-4bbd-8ab2-976adcc0b925" />


---

## 2. Write a PL/SQL program to Calculate Sum of First N Natural Numbers

### Program:
```sql
   DECLARE
    N NUMBER := 10;
    SUM NUMBER := 0;
BEGIN
    FOR I IN 1..N LOOP
        SUM := SUM + I;
    END LOOP;

    DBMS_OUTPUT.PUT_LINE('Sum of first ' || N || ' natural numbers is: ' || SUM);
END;
/
```

### Steps:
- Declare a variable `n` and assign a value (e.g., 10).
- Initialize a `sum` variable to 0.
- Use a `WHILE` loop to iterate from 1 to `n`, adding each number to the sum.
- Display the result using `DBMS_OUTPUT.PUT_LINE`.

**Expected Output:**  
<img width="420" height="232" alt="image" src="https://github.com/user-attachments/assets/f2c0b7bc-396d-4c04-9ee5-206d26ba9333" />


---

## 3. Write a PL/SQL program to generate Fibonacci series

### Program:
```sql
   DECLARE
    N NUMBER := 10;
    A NUMBER := 0;
    B NUMBER := 1;
    C NUMBER;
BEGIN
    DBMS_OUTPUT.PUT_LINE('Fibonacci Series:');

    FOR I IN 1..N LOOP
        DBMS_OUTPUT.PUT(A || ' ');
        C := A + B;
        A := B;
        B := C;
    END LOOP;

    DBMS_OUTPUT.NEW_LINE;
END;
/
```

### Steps:
- Declare the variable `n` to indicate how many terms to generate.
- Initialize the first two Fibonacci numbers (0 and 1).
- Use a loop to generate the next terms using the formula `c = a + b`.
- Print each term in the series.

**Expected Output:**  
<img width="400" height="230" alt="image" src="https://github.com/user-attachments/assets/1f8e5f7f-6c1d-42b0-9635-b5463d86d01d" />


---

## 4. Write a PL/SQL Program to display the number in Reverse Order

### Program:
   ```sql
DECLARE
    N NUMBER := 12345;
    REV NUMBER := 0;
    REM NUMBER;
BEGIN
    WHILE N > 0 LOOP
        REM := MOD(N, 10);
        REV := REV * 10 + REM;
        N := TRUNC(N / 10);
    END LOOP;

    DBMS_OUTPUT.PUT_LINE('Reverse Number: ' || REV);
END;
/
```

### Steps:
- Declare a variable `n` and assign a value (e.g., 1535).
- Use a loop to extract each digit using modulo and reverse the number.
- Display the reversed number.

**Expected Output:**  
<img width="415" height="217" alt="image" src="https://github.com/user-attachments/assets/29cebacf-99b3-4472-a085-737f25e80c6b" />


---

## 5. Write a PL/SQL program to find the largest of three numbers

### Program:
```sql
DECLARE
    A NUMBER := 10;
    B NUMBER := 25;
    C NUMBER := 15;
    LARGEST NUMBER;
BEGIN
    IF A > B AND A > C THEN
        LARGEST := A;
    ELSIF B > C THEN
        LARGEST := B;
    ELSE
        LARGEST := C;
    END IF;

    DBMS_OUTPUT.PUT_LINE('Largest number is: ' || LARGEST);
END;
/
```

### Steps:
- Declare three numeric variables `a`, `b`, and `c`.
- Use nested `IF-ELSIF-ELSE` conditions to find the largest among the three.
- Display the largest number.

**Expected Output:**  
<img width="435" height="235" alt="image" src="https://github.com/user-attachments/assets/3e5193ab-79eb-4fd5-ab9f-7fabdb906bfe" />


## RESULT
Thus, the PL/SQL programs using variables, conditionals, and loops were executed successfully.
