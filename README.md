# Masha_ZH_labs
Нетерминалы:

lang -> expr* 
expr -> assign|while_c|fu
assign -> VAR ASSIGN_OP value op_value 
op_value -> (OP value)* 
value -> DIGIT|VAR| br_expr 
br_expr -> BR_O value (op_value)* BR_C 
while_c -> WHILE_KW BR_O value COMP value BR_C DO_KW expr* END_KW 
fu -> fu_one
fu_one -> FU_ONE VAR

Терминалы:

WHILE_KW -> "while"
DO_KW -> "do"
END_KW -> "end"
VAR -> [a-z]+[a-z0-9]*
DIGIT -> 0|[1-9][0-9]*
OP ->[+]|[-]|[\\*]|[/]	
COMP -> "(>)|(<)|(==)|(!=)"
ASSIGN_OP -> "="
BR_O ->"("
BR_C -> ")"
FU_ONE -> "print"
