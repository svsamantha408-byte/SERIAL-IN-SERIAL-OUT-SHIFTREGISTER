# SERIAL-IN-SERIAL-OUT-SHIFTREGISTER

**AIM:**

To implement  SISO Shift Register using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

A shift register is a sequential circuit used to store and move binary data. It consists of flip-flops connected in series, where data shifts from one stage to the next on each clock pulse. The given Verilog code implements a **4-bit Serial-In Parallel-Out (SIPO) shift register**. On every positive edge of the clock, the serial input bit (`sin`) enters the first stage (`q[0]`), and the existing bits shift to `q[1]`, `q[2]`, and `q[3]`. After four clock cycles, four serially entered bits appear together as a parallel output. This type of register is commonly used in communication systems, data conversion, and temporary data storage.


**SISO shift Register**

A Serial-In Serial-Out shift register is a sequential logic circuit that allows data to be shifted in and out one bit at a time in a serial manner. It consists of a cascade of flip-flops connected in series, forming a chain. The input data is applied to the first flip-flop in the chain, and as the clock pulses, the data propagates through the flip-flops, ultimately appearing at the output.

The logic circuit provided below demonstrates a serial-in serial-out (SISO) shift register. It comprises four D flip-flops that are interconnected in a sequential manner. These flip-flops operate synchronously with one another, as they all receive the same clock signal.

![image](https://github.com/naavaneetha/SERIAL-IN-SERIAL-OUT-SHIFTREGISTER/assets/154305477/e81c4072-37f9-46c6-8145-566764b74c3a)

Figure 01 4 Bit SISO Register

The synchronous nature of the flip-flops ensures that the shifting of data occurs in a coordinated manner. When the clock signal rises, the input data is sampled and stored in the first flip-flop. On subsequent clock pulses, the stored data propagates through the flip-flops, moving from one flip-flop to the next.
Each D flip-flop in the circuit has a Data (D) input, a Clock (CLK) input, and an output (Q). The D input represents the data to be loaded into the flip-flop, while the CLK input is connected to the common clock signal. The output (Q) of each flip-flop is connected to the D input of the next flip-flop, forming a cascade.

**Procedure**

1.Open Quartus Prime.

2.Go to File → New Project Wizard.

3.Enter project name (e.g., EXP10_ShiftRegister).

4.Choose a project folder.

5.Skip device selection or choose any FPGA (Cyclone II/III preferred).

6.Finish the wizard.

**PROGRAM**

module EXP10(clk, sin, q);
input clk;
input sin;
output [3:0] q;
reg [3:0] q;
always @(posedge clk)
begin
q[0] <= sin;
q[1] <= q[0];
q[2] <= q[1];
q[3] <= q[2];
end
endmodule


Developed by: Samantha Shree SV 
RegisterNumber: 25017585

*/

**RTL LOGIC FOR SISO Shift Register**
<img width="1920" height="1080" alt="Screenshot (104)" src="https://github.com/user-attachments/assets/c5b77e7e-8b56-410d-bf71-d4b9bc9a60ec" />

**TIMING DIGRAMS FOR SISO Shift Register**
<img width="1920" height="1080" alt="Screenshot (105)" src="https://github.com/user-attachments/assets/68d86afa-5754-447f-aeb4-82aae87d1746" />

**RESULTS**
Thus SISO Shift Register using verilog and validating their functionality using their functional tables is executed.
