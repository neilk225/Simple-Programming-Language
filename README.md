# Simple Programming Language
This repository contains a lexical analyzer, recursive-descent parser, and interpreter for an imperative programming language created by Bassel Arafeh (NJIT/CS280). 
“lex.h’, “lex.cpp”, “val.h”,  “val.cpp”,  “parseInt.h”, “parseInt.cpp”, and EBNF rules supplied by Bassel Arafeh (NJIT/CS280).

***EBNF Notations:***
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
