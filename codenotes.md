# Chapter 1: What is scope

**Program state** The ability to store values and pull values out of variables.

**Scope** These questions speak to the need for a well-defined set of rules for storing variables in some location, and for finding those variables at a later time

**Compilation** Three steps before the code  is executed

**Tokenizing/Lexing:** Breaking up a string of characters into meaningful (to the language) chunks, called tokens var, a, =, 2, and ;

**Lexing** If the tokenizer were to invoke stateful parsing rules to figure out whether a should be considered a distinct token or just part of another token, that would be .

**Parsing:** Taking a stream (array) of tokens and turning it into a tree of nested elements, which collectively represent the grammatical structure of the program. This tree is called an **_"AST" (Abstract Syntax Tree)._**

The tree for var a = 2; might start with a top-level node called VariableDeclaration, with a child node called Identifier (whose value is a), and another child called AssignmentExpression which itself has a child called NumericLiteral (whose value is 2).

**Code-Generation:** The process of taking an _AST_ and turning it into executable code

that there's a way to take our above described _AST_ for var a = 2; and turn it into a set of machine instructions to actually create a variable called a (including reserving memory, etc.), and then store a value into a.

The JS compiler will take the program var a = 2; and compile it first, and then be ready to execute it, usually right away.


## Understanding scope
Cast of characters that interact to process the program var a = 2;


1. **Engine:** Responsible for start-to-finish compilation and execution of our JavaScript program.

2. **Compiler:** One of Engine's friends; handles all the dirty work of parsing and code-generation (see previous section).

3. **Scope:** Another friend of Engine; collects and maintains a look-up list of all the declared identifiers (variables), and enforces a strict set of rules as to how these are accessible to currently executing code.

When you see the program var a = 2;, you most likely think of that as one statement. But that's not how our new friend Engine sees it. In fact, Engine sees two distinct statements, one which Compiler will handle during compilation, and one which Engine will handle during execution.

## Left and right hand

**Lefthand side** Als iets gedeclareerd wordt 'a = 2;'

**Righthand side** Als iets een reference is a = 'leeftijd'

**Refference error:** Als de scoop het niet kan vinden

**Type error:** Hij is wel succelsvol in het vinden maar kan het niet uitvoeren
