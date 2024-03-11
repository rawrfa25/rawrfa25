//module MULTIPLEXER2TO1_CASE_STATEMENT ( A, B, Sel, Z);
//input A, B, Sel;
//output Z;
//
//assign Z= (~Sel&A) | (Sel&B);
//
//endmodule

module MULTIPLEXER2TO1_CASE_STATEMENT ( A, B, Sel, Z);
input A, B, Sel;
output reg Z;

always@ (Sel or A or B);
   case (Sel)
	0:Z = A;
	1:Z = B;
	endcase
	
	
endmodule
