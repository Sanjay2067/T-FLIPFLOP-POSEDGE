# T-FLIPFLOP-POSEDGE

# AIM:

To implement  T flipflop using verilog and validating their functionality using their functional tables

# SOFTWARE REQUIRED:

Quartus prime

# THEORY:

# T Flip-Flop:

T flip-flop is the simplified version of JK flip-flop. It is obtained by connecting the same input ‘T’ to both inputs of JK flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of T flip-flop is shown in the following figure.

![image](https://github.com/naavaneetha/T-FLIPFLOP-POSEDGE/assets/154305477/458a68fe-2d08-4a9d-ac4f-7ae0480ce0bd)

 
This circuit has single input T and two outputs Qtt & Qtt’. The operation of T flip-flop is same as that of JK flip-flop. Here, we considered the inputs of JK flip-flop as J = T and K = T in order to utilize the modified JK flip-flop for 2 combinations of inputs. So, we eliminated the other two combinations of J & K, for which those two values are complement to each other in T flip-flop. The following table shows the state table of T flip-flop.

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, T flip-flop can be used for one of these two functions such as Hold, & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of T flip-flop. Inputs Present State Next State

![image](https://github.com/naavaneetha/T-FLIPFLOP-POSEDGE/assets/154305477/cdd7fb32-539f-4b66-bb8d-f305a153c886)

 
From the above characteristic table, we can directly write the next state equation as Q(t+1)=T′Q(t)+TQ(t)′ ⇒Q(t+1)=T⊕Q(t)

# Procedure:
1. Define Module: Define a Verilog module for the T flip-flop with inputs (T, CLK) and outputs (Q, Q_bar).

2. Declare Inputs and Outputs: Declare input and output ports for the module.

3. Implement Flip-Flop Logic: Write Verilog code to implement the T flip-flop logic based on its functional table. Use a synchronous always @(posedge CLK) block to trigger the flip-flop on the positive edge of the clock signal.

4. Simulate Using Testbench: Write a Verilog testbench to simulate the behavior of the T flip-flop under different input conditions.

5. Apply Input Stimuli: In the testbench, apply various combinations of input stimuli (T, CLK) to cover all possible input states.

6. Verify Output Behavior: Verify that the output behavior of the T flip-flop matches the expected behavior defined by its functional table.

7. Check for Race Conditions: Ensure that there are no race conditions or undefined states in the design by analyzing the timing and sequence of input changes.


# PROGRAM:
```
Program for flipflops and verify its truth table in quartus using Verilog programming.
Developed by: MAGENDRA SANJAY S
RegisterNumber: 24900652
```
```
module Exp_09( input clk, rst_n, input t,
output reg q,
output q_bar
);
always@(posedge clk) 
begin 
	if(!rst_n)
		q <= 0;
		else
			if(t)
				q <= ~q;
			else
				q <= q;
end
assign q_bar = ~q;
endmodule
```

# RTL LOGIC FOR FLIPFLOPS:
![327636347-757c5394-fe3d-44ee-b064-03cd94608bdc](https://github.com/amirthaviswanathan05/T-FLIPFLOP-POSEDGE/assets/149035397/ae0ed225-d90a-4506-8644-11e70391fda0)

# TIMING DIGRAMS FOR FLIP FLOPS:
![327636373-a3b570d9-f634-4fb5-8691-a3e4de635ca8](https://github.com/amirthaviswanathan05/T-FLIPFLOP-POSEDGE/assets/149035397/b06380e8-0ebb-45be-bca8-aead75835ef0)

# RESULTS:
Thus the program to implement a T flipflop using verilog and validating their functionality using their functional tables is successfully completed.
