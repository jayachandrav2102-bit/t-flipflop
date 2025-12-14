AIM:

To implement T flipflop using verilog and validating their functionality using their functional tables


SOFTWARE REQUIRED:

Quartus prime


THEORY

A T Flip-Flop is a sequential circuit that changes (toggles) its output state on every triggering clock edge if the T input is high (1).

Inputs: T (Toggle), CLK (Clock)

Outputs: Q (Current state), Q’ (Complement of Q)

If T = 0, the flip-flop holds its state.

If T = 1, the flip-flop toggles its state on the clock edge.

Procedure

1.Open your Verilog IDE (Xilinx ISE/Vivado).

2.Create a new project and add a Verilog module named t_flipflop.

3.Declare inputs T and CLK, and outputs Q and Q’.

4.Implement the toggle behavior using an always block triggered by posedge CLK.

5.Compile and synthesize the design.

6.Simulate using a testbench to apply different T inputs and observe Q and Q’.

7.Verify that Q toggles only when T = 1 at the clock edge.

PROGRAM
~~~
module t_ff (
    input  wire clk, rst, T,
    output reg Q 	  
);

  initial begin
     Q<=1'b0;
	 end
  
  
	 always @(posedge clk or posedge rst) begin
	
        if (rst)
            Q <= 1'b0;       // Reset
        else if (T)
            Q <= ~Q;         // Toggle if T=1
        else
            Q <= Q;          // Hold if T=0
    end
endmodule


 Developed by: JAYACHANDRA V
 RegisterNumber:25017587 */
~~~
 
RTL LOGIC FOR FLIPFLOPS

TIMING DIGRAMS FOR FLIP FLOPS

RESULTS: 

Thus the T flipflop using verilog and validating their functionality using their functional tables is implemented and verified.
