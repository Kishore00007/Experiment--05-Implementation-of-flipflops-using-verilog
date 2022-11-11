# Experiment--05-Implementation-of-flipflops-using-verilog
## AIM: 
To implement all the flipflops using verilog and validating their functionality using their functional tables
## HARDWARE REQUIRED:
PC, Cyclone II , USB flasher
## SOFTWARE REQUIRED: 
Quartus prime.
## THEORY: 
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

## Procedure:
1. Open Quartus II and select new project and choose the file location.
2. Module Declaration. Module should have the file name.
3. Declare Inputs and outputs.
4. Use assign declaration and wire to define the functionality of logic circuits.
5. End the program with endmodule.
6. Run the program and choose RTL viewer to get RTL realization.

## PROGRAM: 
```

Program for flipflops  and verify its truth table in quartus using Verilog programming.
Developed by: Kishore Kumar S
RegisterNumber:  212221240023


i) SR FLIP FLOP:

module S(S,R,Clock,Q,Qbar);
input S,R,Clock;
output Q,Qbar;
wire X,Y;
nand (X,S,Clock);
nand (Y,R,Clock);
nand (Q,X,Qbar);
nand(Qbar,Y,Q);
endmodule

ii) D FLIP FLOP:

module D(D,Clock,Q,Qbar);
input D,Clock;
output Q,Qbar;
assign Dbar = ~D;
wire X,Y;
nand (X,D,Clock);
nand (Y,Dbar,Clock);
nand (Q,X,Qbar);
nand (Qbar,Y,Q);
endmodule

iii) JK FLIP FLOP:

module JK(J,K,Clock,Q,Qbar);
input J,K,Clock;
output Q,Qbar;
wire P,S;
nand (P,J,Clock,Qbar);
nand (S,K,Clock,Q);
nand (Q,P,Qbar);
nand (Qbar,S,Q);
endmodule

iv) T FLIP FLOP:

module T (T,Clock,Q,Qbar);
input T,Clock;
output Q,Qbar;
wire A,B;
nand (A,T,Clock,Qbar);
nand (B,T,Clock,Q);
nand (Q,A,Qbar);
nand (Qbar,B,Q);
endmodule

```

## RTL LOGIC FOR FLIPFLOPS :
### SR Flip Flop:
![image](https://user-images.githubusercontent.com/94233985/201400272-91437c93-16af-4676-be01-d8c013d80f23.png)
### D Flip Flop:
![image](https://user-images.githubusercontent.com/94233985/201400551-996ff940-f5c4-4c88-a10c-5cca6ea6c17c.png)
### JK Flip Flop:
![image](https://user-images.githubusercontent.com/94233985/201400605-57a29829-1c93-4abb-a121-573239fa8296.png)
### T Flip Flop:

![image](https://user-images.githubusercontent.com/94233985/201400643-8c01838d-10db-4993-8080-e796df859439.png)
## TIMING DIGRAMS FOR FLIP FLOPS:
### SR Flip Flop:
![image](https://user-images.githubusercontent.com/94233985/201400694-e5b38673-4703-4e2a-b8f0-b8c9d315950d.png)
### D Flip FLop:
![image](https://user-images.githubusercontent.com/94233985/201400728-3266233a-6082-4d70-b632-ae326cdeaa1b.png)
### JK FLip Flop:

![image](https://user-images.githubusercontent.com/94233985/201400778-37ac3b32-9c5a-4593-a6e9-f832f20a7c67.png)

### T Flip Flop:
![image](https://user-images.githubusercontent.com/94233985/201400811-82b9a97a-fa92-4039-b1e8-1a7f849cec3a.png)



## RESULTS:
All the flipflops are implementde using verilog and their functionality has been validated using their functional tables.


