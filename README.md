# RTl-to-GDS-ASIC-Design-Flow

Problem Statement and Design Steps

Following design steps are completed.
1. Made a detailed specification of the problem.

[1] Input ports: [3:0]A, [12:0]B, [5:0]C, clk, rst. A and B are data lines and C is control line

[2] Output port: [7:0] OUT

[3] Four functions need to be implemented by design:

  I. BCD Counter: C=6’o00 to 6’o14
  
  II. 1x8 DeMux: C=6’o15 to 6’o30
  
  III. 4 bit even parity generator: C=6’o31 to 6’o46
  
  IV. A+B[12:10]: C=6’o47 to 6’o77

   
2. Write Verilog code for the design meeting the above specification.
Develop Testbench that simulates the above Verilog design and compares the results with the 
given specification.
Three different testbenches need to be written, with different code-coverages. Simulation
needs to be carried out for all the three testbenches and coverage computed for all three
testbenches.
You need to study the impact of test-vectors on code-coverage.
Put your final analyses in the report.

3. Synthesize the design using three different constraints. Three different constraints should be
as follows:
  a. Synthesize for minimum area, keeping timing constraints highly relaxed.
  b. Synthesize for best timing, keep timing constraints tight. Keep making the timing
constraints tighter unless you observe a negative slack. The timing analysis should
show slight negative slack for this constraint.
  c. Synthesize for timing constraints that is between (a) and (b) above.
You need to study the impact of changing the constraints on the QoR.
Also try to understand what portion of the code in RTL corresponds to which all instances in
the netlist. Put your explanation in the final report.

4. Do formal equivalence checking of the generated netlists in 3 (a)-(c) and the Verilog code.
Manually make a change in the netlist (let us call it bad-netlist) to make it non-equivalent with
the RTL. Study the failure for this netlist and analyse the result.
Note down different error messages that are reported by the formal equivalence tool. Try to
make bad-netlist in several different ways and list out different types of error messages
reported by Formal Equivalence Tool.

5. Perform Static Timing Analysis (STA) of the netlists generated in 3 (a)-(c)
Use the same constraint file that was employed in 3(c) for performing STA of all three netlists
generated in 3 (a)-(c).
Analyze and interpret the slack obtained in all the three netlists.
Analyze the timing report generated for different timing paths by the tools. Explain different
fields that appear in the timing report and how are they computed.

6. Test insertion:
Insert a single scan chain in the synthesized designs using RTL Compiler or Design Compiler
Save the netlist that has scan-chain inserted.
Explain the purpose of all the new entities that appear in the scan-chain inserted netlist.
With the scan-chain inserted netlist, explain how the netlist will be used to detect failures.
Report area and timing for scan-inserted netlists and compare with the result for netlist that
has no scan chain.
Explain the reason for difference in QoR for both timing and area.
Take a detailed timing report of a same path in the original netlist and the scan-chain inserted
netlist. Explain the difference in QoR by observing the effect of scan-insertion on different
fields of the timing report.

7.Following design steps need to be completed
  1. Floorplanning
  2. Power Network Design
  3. Placement
  4. Clock-Tree Synthesis
  5. Routing
  6. Writing out final GDS

  1. Floorplanning is done with small utilization (say 0.5) or large die area
  2. Floorplanning is done with large utilization (say 0.8) or small die area
