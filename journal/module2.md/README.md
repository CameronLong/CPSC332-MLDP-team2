# Grammar Design Reflection – Cameron Long, Jenny LaFlair, Julian Davis, Kaylie Marshall

## What grammar rules did you sketch for your proposed language?
For our proposed language, we designed grammar rules to support basic program structure, variable declarations, assignments, arithmetic expressions, and output statements.

## Did you identify any ambiguities or left recursion?
Yes, we identified left recursion in the expr rule. The rule references itself at the beginning of multiple alternatives, such as:

expr: expr ('+'|'-') expr

This creates left recursion, which can be problematic in some parsing techniques. Additionally, we noticed potential ambiguity in arithmetic expressions if operator precedence is not clearly defined (for example, 3 + 4 * 5).

## How did ANTLR handle your grammar?
ANTLR was able to process the grammar, but it highlighted the importance of structuring expression rules carefully. In some cases, adjustments may be needed to clearly define precedence and avoid confusion.

Running the grammar in ANTLR helped verify that the parser could recognize valid statements such as variable declarations and print expressions. It also made it easier to identify areas where the grammar could be improved.

## What did you learn about syntax definition or parser behavior?

We learned that defining syntax requires precision, especially when dealing with recursive rules and expressions. Small changes in grammar structure can significantly affect how a parser interprets input.

We also learned that ambiguity in grammar can lead to unclear parsing results, so it is important to explicitly define operator precedence and structure. Using ANTLR provided useful feedback and helped us better understand how parsers analyze and interpret language rules.

## ANTLR Test Notes

We tested the grammar using sample input programs that included variable declarations, assignments, and print statements. The parser successfully recognized the structure of these programs.

Testing also showed that expression handling requires careful design to ensure correct evaluation order, reinforcing the need to refine grammar rules.

Below is a simplified version of our grammar:

```antlr
program: statement+ ;

statement
    : varDecl
    | assignment
    | printStmt
    ;

varDecl: 'let' ID '=' expr ';' ;
assignment: ID '=' expr ';' ;

printStmt: 'print' '(' expr ')' ';' ;

expr
    : expr ('*'|'/') expr
    | expr ('+'|'-') expr
    | INT
    | ID
    | '(' expr ')'
    ;

