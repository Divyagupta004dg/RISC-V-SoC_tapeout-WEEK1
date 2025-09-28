🟢 Conditional Execution with If-Else in Verilog

If-else statements are used to model decisions in behavioral code inside procedural blocks (always, initial, tasks, or functions).

● Syntax pattern

``if (condition) begin  
   // Executes if condition is true  
end else begin  
   // Executes if condition is false  
end``


● Key points

condition → Any expression that evaluates to true (non-zero) or false (zero).

begin ... end → Required when multiple statements are grouped; not needed for a single statement.

else → Optional; can be omitted if only the true case matters.

● Nested conditions

``if (cond1) begin  
   // Action if cond1 is true  
end else if (cond2) begin  
   // Action if cond2 is true  
end else begin  
   // Action if neither condition holds  
end``

🟢 Inferred Latches in Verilog

When writing combinational logic, if all possible input conditions don’t assign a value, synthesis tools automatically create a latch to “remember” the previous value. This is often unintentional.

● Example – Latch Created

``module ex (
    input wire a, b, sel,
    output reg y
);
    always @(a, b, sel) begin
        if (sel == 1'b1)
            y = a;   // Missing else → y not updated when sel=0
    end
endmodule``


👉 Problem: y is left unassigned when sel=0, so a latch is inferred.


● Fix – Provide Else or Default Assignment

``module ex (
    input wire a, b, sel,
    output reg y
);
    always @(a, b, sel) begin
        case(sel)
            1'b1    : y = a;
            default : y = 1'b0;  // Safe default prevents latch
        endcase
    end
endmodule``

👉 Solution: Always cover all branches (else/default) to prevent unintended latch inference.
