You have to solve the following two problems using stack data structure and the algorithms taught in the class ( uploaded note/slides: L03_onward_CASD_ATT_21Aug_2020.pdf ).

Q1: Write a C/C++ program to convert an infix expression to the equivalent postfix expression.
Input specification: The input infix expression consists of a sequence of tokens, where a token may be of the following types:
   i) arithmetic operators: +,-, *, /, ^, and, % (respectively called the addition, subtraction, multiplication, division, exponentiation, and modulo) which are arranged in the increasing order of their priorities.
   ii) Operands: floating point numbers, variables (alpha-numeric string starting with a letter from English alphabet (case sensitive)).
  iii) There may or may not be any space between two tokens in the expression. Read input infix expression  from the command prompt.
   
Output specification: Equivalent postfix expression where consecutive tokens are separated by a single space.  Write the output on computer screen (standard out).
Example 1 Infix: A * B % C+(D+E-F)/G^(H / I*J)  
                    Equivalent Postfix: A B C % * D E + F - H I / J * G ^ / +

Example 2 Infix: 10 *50% count+(var1+3.8-a231)/ ex^(deg / 20.4*k)  
                    Equivalent Postfix: 10 50 count % * var1 3.8 + a231 - deg 20.4 / k * ex ^ / +

Example 3 Infix: 5*20%7 + (13+14.250-7.25)/2.0^(4.0/20.50*10.25) 
                    Equivalent Postfix: 5 20 7 % * 13 14.250 + 7.25 - 4.0 20.50 / 10.25 * 2.4 ^ / +

Q2. Write a C/C++ program to evaluate a postfix expression where all operands in the expression are numeric values.  The input specification is same as in the Q1. The input is an infix expression, first your program should convert it to the equivalent postfix expression. You may use your solution program of Q1 for this.  Next, your should evaluate the postfix expression and write on the screen.  Read input infix expression  from the command prompt.
 Example 5 input Infix: 5*20%7 + (13+14.250-7.25)/2.0^(4.0/20.50*10.25) 
                     Equivalent Posfix: 5 20 7 % * 13 14.250 + 7.25 - 4.0 20.50 / 10.25 * 2.4 ^ / +
                     Expected output: 35 (value of this expression)

    Example 6: Infix Expression: 5 ∗ (6 + 2) − 12/4
                         Equivalent Postfix Expression: 5 6 2 + ∗ 12 4 / −   (space separated)
                         Value: 37

Submission: A zipped file containing a readme file and the source programs for solving Q1 and Q2. The .zip file name should be A<your name>_<student ID>_A02.zip. For example, if your name is "Ananda Das" and your student ID is 1125, then the zip file name should be Anand_Das_1125_A02.zip

Hints: You many read the infix expression from a file and write the result to another file.
In either case, the the whole infix expression in an array of character. Scan from the beginning (left to right) and extract a token. A token is either an arithmetic operator or an word. An word alphanumeric---where a variable is an word starting with a any of the character 'A' to 'Z ' or 'a' to 'z' or an '_' (under-score); a word could be a numeric value (integer or floating point number) which consists of digits from 0 to 9 and decimal point. Another type of token is a parenthesis: '(' and ')'.
Write a function that extract these tokens from the input. Then, you can utilize it in your main program.
