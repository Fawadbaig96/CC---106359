MiniJava Compiler
**106359**
###PROJECT MEMBERS###
StdID | Name
------------ | -------------
**63358** | **Sameen Azhar** 
62669 | Mirza Fawad Baig

## Project Description ##
Our project was to make a compiler and parse a simple program. We chose MiniJava as our language and tried to make lexical analyzer and a parser in which we succeed on making Lexical analyzer but not a parser. 

## MiniJava ##
MiniJava is used for compiler construction. The language contains only few statements as well as expressions and requires only a simple run-time system. It does not include giving exceptions and multi-threading.

## Sample Code ##
```Java

public class HelloWorld {

    public static void main(String[] args) {
        // Prints "Hello, World" to the terminal window.
        System.out.println("Hello, World");
    }

}

```
##Lexical Specification##

• White space: These are space, new line, carriage return and tabulator

• Comments: The string /* followed by any characters until the terminating / is a comment. Comments are not nestable, further / within a comment are ignored, a comment always ends when the first */ is encountered.

• Keywords and operators, all tokens printed in bold in the grammar specification are keywords or operators. Exceptions are main, String, System, Out, and println. There are identifiers, not keywords.

• IDENT: An identifier starts with an underscore or letter and is followed by anynumber of letters, underscores and digits. Only the letters A to Z and a to z are allowed, case is important. Keywords are not IDENTs.

• INTEGER_LITERAL: A decimal integer literal is a digit sequence starting with any of the digits 1 to 9 and is followed by any number of digits 0 to 9. A single 0 is also an integer literal.

Comments and white space have no meaning except for separating tokens.

###Grammar###

MiniJava Grammar Program ::= MainClass ( ClassDeclaration )* MainClass ::= "class" Identifier "{" "public" "static" "void" "main" "(" "String" "[" "]" Identifier ")" "{" Statement "}" "}" ClassDeclaration ::= "class" Identifier ( "extends" Identifier )? "{" ( VarDeclaration )* ( MethodDeclaration )* "}" VarDeclaration ::= Type Identifier ";" MethodDeclaration ::= "public" Type Identifier "(" ( Type Identifier ( "," Type Identifier )* )? ")" "{" ( VarDeclaration )* ( Statement )* "return" Expression ";" "}" Type ::= "int" "[" "]" | "boolean" | "int" | Identifier Statement ::= "{" ( Statement )* "}" | "if" "(" Expression ")" Statement "else" Statement | "while" "(" Expression ")" Statement | "System.out.println" "(" Expression ")" ";" | Identifier "=" Expression ";" | Identifier "[" Expression "]" "=" Expression ";" Expression ::= Expression ( "&&" | "<" | "+" | "-" | "" ) Expression | Expression "[" Expression "]" | Expression "." "length" | Expression "." Identifier "(" ( Expression ( "," Expression ) )? ")" | <INTEGER_LITERAL> | "true" | "false" | Identifier | "this" | "new" "int" "[" Expression "]" | "new" Identifier "(" ")" | "!" Expression | "(" Expression ")" Identifier ::=

Sample program class Factorial{ public static void main(String[] a){ System.out.println(new Fac().ComputeFac(10)); } }

class Fac { public int ComputeFac(int num){ int num_aux ; if (num < 1) num_aux = 1 ; else num_aux = num * (this.ComputeFac(num-1)) ; return num_aux ; } }

##Problems Faced##
We faced a bunch of problems. By looking at Mr.Farooq Zaidi videos multiple times and took help from internet we made a lexical analyzer although our final phase also to make a parser. We watched several videos on YouTube and also Googled it but couldn't find any. We tried our best.

###Problem 1: How does Lexical Analyzer work?###
 
By watching Sir Farooq Zaidi videos and looking at his lectures, we found out that it tokenizes the code one by one and creates a token stream.

###Problem 2: YACC###
We took a help from github members, copied their code, made some changes, it is compiling correctly. Not giving any errors but when we are passing a syntax, it's giving a syntax error. We couldn't find any solution to it.

##References##
- [links](https://youtu.be/54bo1qaHAfk), YouTube video 1.
- [links](https://youtu.be/__-wUHG2rfM), YouTube video 2.
- [links](https://github.com/starbops/MJP), Github Link.
- You see markdown is not that difficult.
- You are CS students not some tom harry from BBA SHE-B-A :-).