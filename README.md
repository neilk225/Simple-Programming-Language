# Simple-Programming-Language
The following is a simple programming language abdiding by specific EBNF notation and implemented through the means of a lexical analyzer, parser, and interpreter.  “lex.h’, “lex.cpp”, “val.h”,  “val.cpp”,  “parseInt.h”, “parseInt.cpp”, and EBNF rules supplied by Bassel Arafeh (NJIT/CS280).

###***EBNF Notations:***
- Prog ::= PROGRAM IDENT StmtList END PROGRAM  
- DeclStmt ::= (INT | FLOAT) IdentList  
- IdentList ::= IDENT, {, IDENT}  
- StmtList ::= Stmt; {Stmt;} 
- Stmt ::= DeclStmt | ControlStmt  
- ControlStmt ::= AssigStmt | IfStmt | WriteStmt  
- WriteStmt ::= WRITE ExprList 
- IfStmt ::= IF (LogicExpr) ControlStmt 
- AssignStmt ::= Var = Expr 
- ExprList ::= Expr {, Expr} 
- Expr ::= Term {(+|-) Term} 
- Term ::= SFactor {( *| / | % ) SFactor}  
- SFactor ::= (+ | -) Factor | Factor 
- LogicExpr ::= Expr (== | >) Expr 
- Var ::= IDENT 
- Factor = IDENT | ICONST | RCONST | SCONST | (Expr)
