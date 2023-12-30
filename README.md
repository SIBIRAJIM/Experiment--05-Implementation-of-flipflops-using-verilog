## NAME :SIBIRAJI M
## REG NO: 212223050048

## Experiment--05-Implementation-of-flipflops-using-verilog
### AIM: To implement all the flipflops using verilog and validating their functionality using their functional tables
### HARDWARE REQUIRED:  – PC, Cyclone II , USB flasher
### SOFTWARE REQUIRED:   Quartus prime
### THEORY 
SR Flip-Flop
SR flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, SR latch operates with enable signal. The circuit diagram of SR flip-flop is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167910294-bb550548-b1dc-4cba-9044-31d9037d476b.png)

 
This circuit has two inputs S & R and two outputs Qtt & Qtt’. The operation of SR flipflop is similar to SR Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of SR flip-flop.


![image](https://user-images.githubusercontent.com/36288975/167910648-ced88e69-869c-42e2-9718-a285a3902446.png)


Here, Qtt & Qt+1t+1 are present state & next state respectively. So, SR flip-flop can be used for one of these three functions such as Hold, Reset & Set based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of SR flip-flop.
Present Inputs	Present State	Next State


![image](https://user-images.githubusercontent.com/36288975/167908180-5fc9d589-1cb5-41f5-b2c8-927e04f5f387.png)

By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. The three variable K-Map for next state, Qt+1t+1 is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167908214-25b30a54-db20-4bcb-9385-5f93a1982a09.png)

 
The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=S+R′Q(t)Q(t+1)=S+R′Q(t)


### D Flip-Flop
D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.
 
This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of D flip-flop.
![image](https://user-images.githubusercontent.com/36288975/167908342-e03f0cbb-5958-43bb-b74a-5e3ec2341675.png)

![image](https://user-images.githubusercontent.com/36288975/167910325-aeef0739-0a54-40e2-bebd-6f5fa0cad10e.png)



Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as
Qt+1t+1 = D



![image](https://user-images.githubusercontent.com/36288975/167908850-d39d07ba-7f9d-490a-b9f2-274e189fd047.png)

Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.


### JK Flip-Flop
JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure.
![image](https://user-images.githubusercontent.com/36288975/167910378-d2d984a7-2815-4d17-8c41-ee4bdf59ec24.png) 

 
This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs.
The following table shows the state table of JK flip-flop.


![image](https://user-images.githubusercontent.com/36288975/167908575-59c35afb-50d3-46a2-888c-47478a3179d5.png)

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop.
Present Inputs	Present State	Next State

![image](https://user-images.githubusercontent.com/36288975/167908664-c854ffe9-0bd3-44c2-bfa6-e53928181c69.png)


By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.
 
 
 ![image](https://user-images.githubusercontent.com/36288975/167908688-fa93c3e9-8323-4864-947d-c11d163d5a90.png)

The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)



### T Flip-Flop
T flip-flop is the simplified version of JK flip-flop. It is obtained by connecting the same input ‘T’ to both inputs of JK flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of T flip-flop is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167911534-5f3c445d-bc68-46e2-9a9c-7efce5febc60.png)



This circuit has single input T and two outputs Qtt & Qtt’. The operation of T flip-flop is same as that of JK flip-flop. Here, we considered the inputs of JK flip-flop as J = T and K = T in order to utilize the modified JK flip-flop for 2 combinations of inputs. So, we eliminated the other two combinations of J & K, for which those two values are complement to each other in T flip-flop.
The following table shows the state table of T flip-flop.



Here, Qtt & Qt+1t+1 are present state & next state respectively. So, T flip-flop can be used for one of these two functions such as Hold, & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of T flip-flop.
Inputs	Present State	Next State


![image](https://user-images.githubusercontent.com/36288975/167909015-53aa9450-3f28-4202-887a-79d88228f8a0.png)

From the above characteristic table, we can directly write the next state equation as
Q(t+1)=T′Q(t)+TQ(t)′
⇒Q(t+1)=T⊕Q(t)

## Procedure
1. Create a New Project:
   - Open Quartus and create a new project by selecting "File" > "New Project Wizard."
   - Follow the wizard's instructions to set up your project, including specifying the project name, location, and target device (FPGA).

2. Create a New Design File:
   - Once the project is created, right-click on the project name in the Project Navigator and select "Add New File."
   - Choose "Verilog HDL File" or "VHDL File," depending on your chosen hardware description language.

3. Write the Combinational Logic Code:
   - Open the newly created Verilog or VHDL file and write the code for your combinational logic.
     
4. Compile the Project:
   - To compile the project, click on "Processing" > "Start Compilation" in the menu.
   - Quartus will analyze your code, synthesize it into a netlist, and perform optimizations based on your target FPGA device.

5. Analyze and Fix Errors:
   - If there are any errors or warnings during the compilation process, Quartus will display them in the Messages window.
   - Review and fix any issues in your code if necessary.
   - View the RTL diagram.

6. Verification:
   - Click on "File" > "New" > "Verification/Debugging Files" > "University Program VWF".
   - Once Waveform is created Right Click on the Input/Output Panel > " Insert Node or Bus" > Click on Node Finder > Click On "List" > Select All.
   - Give the Input Combinations according to the Truth Table amd then simulate the Output Waveform.



## PROGRAM 
Program for flipflops  and verify its truth table in quartus using Verilog programming.

# SR-Flip 
![Screenshot 2023-12-29 091258](https://github.com/SIBIRAJIM/Experiment--05-Implementation-of-flipflops-using-verilog/assets/154588445/9f9a8018-5484-4f2f-a80c-7bf890eeff72)
Flop

### JK Flip-Flop
![Screenshot 2023-12-29 091401](https://github.com/SIBIRAJIM/Experiment--05-Implementation-of-flipflops-using-verilog/assets/154588445/4a88ad9e-3230-41aa-b784-48b3b940d0c3)

### D Flip-Flop
![Screenshot 2023-12-29 091449](https://github.com/SIBIRAJIM/Experiment--05-Implementation-of-flipflops-using-verilog/assets/154588445/c37081af-b9b6-47f9-9888-a495bcbd3677)

### T Flip-Flop
![Screenshot 2023-12-29 091716](https://github.com/SIBIRAJIM/Experiment--05-Implementation-of-flipflops-using-verilog/assets/154588445/6458d85b-c25d-465d-b7f9-9af48eb061e3)

## RTL LOGIC FOR FLIPFLOPS 

### SR Flip-Flop
![Screenshot 2023-12-15 142814](https://github.com/SIBIRAJIM/Experiment--05-Implementation-of-flipflops-using-verilog/assets/154588445/f877c44d-67ba-4c6d-9b30-20b8c2afa54c)

### JK Flip-Flop
![Screenshot 2023-12-15 142439](https://github.com/SIBIRAJIM/Experiment--05-Implementation-of-flipflops-using-verilog/assets/154588445/5e3bf039-0b58-4fc3-947f-eef3f69b1134)

### D Flip-Flop
![Screenshot 2023-12-15 140300](https://github.com/SIBIRAJIM/Experiment--05-Implementation-of-flipflops-using-verilog/assets/154588445/f136bdc8-9876-49f2-91d2-abbb323a302e)

### T Flip-Flop
![Screenshot 2023-12-15 142001](https://github.com/SIBIRAJIM/Experiment--05-Implementation-of-flipflops-using-verilog/assets/154588445/085fadc4-a998-4406-ab3a-5016edf08622)


## TIMING DIGRAMS FOR FLIP FLOPS 

### SR Flip-Flop
![Screenshot 2023-12-22 141151](https://github.com/SIBIRAJIM/Experiment--05-Implementation-of-flipflops-using-verilog/assets/154588445/45ffaece-6201-4b65-a1f4-16eb3b7c904d)

### JK Flip-Flop
![Screenshot 2023-12-15 142651](https://github.com/SIBIRAJIM/Experiment--05-Implementation-of-flipflops-using-verilog/assets/154588445/de59544f-13c2-4015-8d28-648a187188ec)

### D Flip-Flop
![Screenshot 2023-12-15 140504](https://github.com/SIBIRAJIM/Experiment--05-Implementation-of-flipflops-using-verilog/assets/154588445/152256eb-3271-483c-a0be-f24491be1f10)

### T Flip-Flop
![Screenshot 2023-12-15 142237](https://github.com/SIBIRAJIM/Experiment--05-Implementation-of-flipflops-using-verilog/assets/154588445/915b37a6-451d-4566-9a3f-1e8d152f03c9)


### RESULTS 
By this we have verified the truth table of SR, JK, D and T using verilog.







