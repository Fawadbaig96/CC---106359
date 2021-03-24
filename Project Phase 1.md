# CC Spring 2021: Project Phase 1
### PROJECT MEMBERS ###
StdID | Name
------------ | -------------
**63358** | **Sameen Azhar** 
62669 | Mirza Fawad Baig  

## Language Selected ##
Mini Java

## Example of main constructs ##

 public static void main(String[] args)
 
## Example of for loop constructs ##
 
 class ForLoopExample {
 
    public static void main(String args[]){
    
         for(int i=10; i>1; i--){
         
              System.out.println("The value of i is: "+i);
         }
    }
}

## Example of array constructs ##

 int arr[]={2,11,45,9};

## Example of if else condition constructs ##

public class IfElseExample {

   public static void main(String args[]){
    
    int num=120;
     if( num < 50 ){
	System.out.println("num is less than 50");
     }
     else {
	System.out.println("num is greater than or equal 50");
     }
   }
}

## Example of while loop constructs ##

int a = 100;

while(a > 0)
{
    // Do something

    a = a - 1;
}


## Context-free grammar for Mini-Java ##

A context-free grammar consists of a number of productions. Each production has an abstract symbol called a nonterminal as its left-hand side, and a sequence of one or more nonterminal and terminal symbols as its right-hand side. For each grammar, the terminal symbols are drawn from a specified alphabet.

Starting from a sentence consisting of a single distinguished nonterminal, called the goal symbol, a given context-free grammar specifies a language, namely, the set of possible sequences of terminal symbols that can result from repeatedly replacing any nonterminal in the sequence with a right-hand side of a production for which the nonterminal is the left-hand side.


In MiniJava we accept identifiers consisting of ASCII characters only, integer literals including octal and hexadecimal, and character and string literals consisting of ASCII characters only, and including escapes.
Types
Type:
	PrimitiveType
	ReferenceType
PrimitiveType:
	int
	boolean
ReferenceType:
	ClassType
	ArrayType
ClassType:
	Name
ArrayType:
	PrimitiveType [ ]
	ClassType [ ]
	ArrayType [ ]
Names
Name:
	SimpleName
	QualifiedName
SimpleName:
	Identifier
QualifiedName:
	Name . Identifier
Packages
CompilationUnit:
	TypeDeclaration*
TypeDeclaration:
	ClassDeclaration
	;
Modifiers
Modifiers:
	Modifier*
Modifier:
	public
	static
	native
Classes
Class Declaration
ClassDeclaration:
	class Identifier Superopt ClassBody
Super:
	extends ClassType
ClassBody:
	{ ClassMemberDeclaration* }
ClassMemberDeclaration:
	FieldDeclaration
	MethodDeclaration
Field Declarations
FieldDeclaration:
	Modifiers Type IdentifierList ;
IdentifierList:
	Identifier
	IdentifierList , Identifier
Method Declarations
MethodDeclaration:
	MethodHeader MethodBody
MethodHeader:
	Modifiers Type MethodDeclarator Throwsopt
	Modifiers void MethodDeclarator Throwsopt
MethodDeclarator:
	Identifier ( FormalParameterListopt )
FormalParameterList:
	FormalParameter
	FormalParameterList , FormalParameter
FormalParameter:
	Type Identifier
Throws:
	throws ClassType
MethodBody:
	Block
	;
Blocks and Statements
Block:
	{ BlockStatement* }
BlockStatement:
	LocalVariableDeclarationStatement
	Statement
LocalVariableDeclarationStatement:
	LocalVariableDeclaration ;
LocalVariableDeclaration:
	Type VariableDeclarators
VariableDeclarators:
	VariableDeclarator
	VariableDeclarators , VariableDeclarator
VariableDeclarator:
	Identifier
	Identifier = Expression
Statement:
	Block
	ExpressionStatement
	IfThenStatement
	IfThenElseStatement
	WhileStatement
	DoWhileStatement
	ReturnStatement
	BreakStatement
	ContinueStatement
	ForStatement
ExpressionStatement:
	StatementExpressionopt ;
StatementExpression:
	Expression
IfThenStatement:
	if ( Expression ) Statement
IfThenElseStatement:
	if ( Expression ) Statement else Statement
WhileStatement:
	while ( Expression ) Statement
DoWhileStatement:
	do Statement while ( Expression ) ;
ReturnStatement:
	return Expressionopt ;
BreakStatement:
	break ;
ContinueStatement:
	continue ;
ForStatement:
	for ( ForInitopt ; Expressionopt ; ForUpdateopt ) Statement
ForInit:
	StatementExpressionList
	LocalVariableDeclaration
ForUpdate:
	StatementExpressionList
StatementExpressionList:
	StatementExpression
	StatementExpressionList , StatementExpression
Expressions
Expression:
	ConditionalExpression
	AssignmentExpression
AssignmentExpression:
	ConditionalExpression = Expression
ConditionalExpression:
	InfixExpression
	InfixExpression ? Expression : ConditionalExpression
InfixExpression:
	PrefixExpression
	InfixExpression InfixOp PrefixExpression
InfixOp:
	||
	&&
	==
	!=
	<
	>
	<=
	>=
	+
	-
	*
	/
PrefixExpression:
	PrefixOp PrefixExpression
	PostfixExpression
PrefixOp:
	-
	!
PostfixExpression:
	Primary Suffix*
Suffix:
	ArrayAccess
	FieldAccess
	MethodInvocation
ArrayAccess:
	[ Expression ]
Selector:
	. Identifier
FieldAccess:
	Selector
MethodInvocation:
	Selector ( ArgumentListopt )
ArgumentList:
	Expression
	ArgumentList , Expression
Primary:
	( Expression )
	this
	Literal
	Identifier
	super FieldAccess
	super MethodInvocation
	ClassInstanceCreationExpression
	ArrayCreationExpression
ClassInstanceCreationExpression:
	new ClassType ( )
ArrayCreationExpression:
	new PrimitiveType [ Expression ] Dimension*
	new ClassType [ Expression ] Dimension*
Dimension:
	[ ]
