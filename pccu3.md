Here’s a detailed explanation of the topics related to syntax specification and parsing techniques for your viva:


---

Specification of Syntax Using Grammar

The syntax of a programming language is specified using context-free grammar (CFG). CFG consists of:

1. Terminals: Basic symbols (e.g., keywords, operators) that form the actual syntax.


2. Non-terminals: Abstract symbols representing language constructs (e.g., <expression>, <statement>).


3. Start Symbol: A special non-terminal from which parsing begins.


4. Production Rules: Rules defining how non-terminals are replaced by terminals and/or other non-terminals.



Example Grammar: For arithmetic expressions:

<expression> → <expression> + <term> | <term>
<term> → <term> * <factor> | <factor>
<factor> → ( <expression> ) | id

Derivation: Given the input id + id * id, derivation proceeds as:

1. <expression> → <expression> + <term>


2. <expression> → <term> + <term>


3. <term> → <factor>


4. <factor> → id ... and so on.




---

Top-Down Parsing

Top-down parsing starts at the root (start symbol) and tries to derive the input string by recursively expanding production rules.

1. Recursive-Descent Parsing

A manual approach to top-down parsing.

Implements one function for each non-terminal.

Uses backtracking if an incorrect rule is chosen.

Inefficient due to backtracking.


Example: For grammar <expression> → <term> + <term>:

Function for <expression> will call the function for <term> and check for +.


2. Predictive Parsing

Eliminates backtracking by using lookahead (peeking at the next input symbol).

Works only for LL(1) grammars (grammars where one lookahead is sufficient).

Uses a parse table to decide which rule to apply.


Steps:

1. Construct a FIRST set (possible tokens at the beginning of a production).


2. Construct a FOLLOW set (possible tokens after a non-terminal).


3. Build a parsing table.




---

Bottom-Up Parsing

Bottom-up parsing starts with the input string and attempts to reduce it to the start symbol by applying grammar rules in reverse.

1. Shift-Reduce Parsing

Shift: Push input symbols onto a stack.

Reduce: Replace the top stack symbols with a non-terminal using a production rule.

Conflicts:

Shift/Reduce Conflict: Parser cannot decide whether to shift or reduce.

Reduce/Reduce Conflict: Parser cannot decide which production to use.



2. Simple LR (SLR) Parsing

Uses an LR(0) automaton and FOLLOW sets to resolve reduce actions.

SLR Table: Combines states from the automaton with grammar rules to guide parsing.


3. Canonical LR (CLR) Parsing

More powerful than SLR.

Uses LR(1) items, which add a lookahead symbol to LR(0) items.

Handles a wider range of grammars but generates larger parsing tables.


4. Look-Ahead LR (LALR) Parsing

Combines the power of CLR and the compactness of SLR.

Merges similar states in the CLR table to create a smaller table.

Widely used in parser generators like YACC.



---

Parser Generator

Parser generators automate the creation of parsers from grammar specifications.

YACC (Yet Another Compiler Compiler)

1. Input: Grammar rules written in a specific format.

Example:

%%
expr : expr '+' term
     | term;
term : term '*' factor
     | factor;
factor : '(' expr ')'
      | ID;
%%



2. Output: A C program that implements the parser.


3. Compilation: Compile the output file into an executable parser.



Advantages:

Saves time in parser development.

Reduces errors compared to manual parser implementation.



---

Summary of Parsing Methods

Let me know if you need examples or further clarification!

