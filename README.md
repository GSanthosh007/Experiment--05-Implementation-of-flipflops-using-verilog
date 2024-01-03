![292614715-4340fbea-cddf-47a4-bb55-f2ab8dfc70ba](https://github.com/GSanthosh007/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147527586/006cf103-07f8-492b-a2be-b7c90921efe4)# Experiment--05-Implementation-of-flipflops-using-verilog
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

### Procedure
/* write all the steps invloved */
![Screenshot 2024-01-03 060134](https://github.com/GSanthosh007/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147527586/719d9241-6bbe-4bcc-9d08-f4a729a36914)

### PROGRAM 
/*
Program for flipflops  and verify its truth table in quartus using Verilog programming.
Developed by: SANTHOSH G
RegisterNumber:212223240152  
*/
1.SR FLIP FLOP:
![Screenshot 2024-01-03 060255](https://github.com/GSanthosh007/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147527586/4b2fd328-3669-4bd0-b1e7-7fc488934a1e)


2.D FLIP FLOP:
![Screenshot 2024-01-03 060312](https://github.com/GSanthosh007/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147527586/8eef2aec-2c20-451a-8673-5b058d2bef17)


3.JK FLIP FLOP:
![Screenshot 2024-01-03 060333](https://github.com/GSanthosh007/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147527586/25aefa6f-121d-4f15-9ca4-884f358b6af6)


4.T FLIP FLOP:
![Screenshot 2024-01-03 060401](https://github.com/GSanthosh007/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147527586/7c12405f-f6f5-4f46-ae27-f4f84b1c81b1)


### RTL DIAGRAM:
SR FLIP FLOP:
![Screenshot 2024-01-03 060428](https://github.com/GSanthosh007/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147527586/9218d98f-0f91-47cd-9c39-66e374e23deb)

D FLIP FLOP:
![Screenshot 2024-01-03 060446](https://github.com/GSanthosh007/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147527586/a337055e-3059-468f-ba8e-cb1f73595930)


JK FLIP FLOP:
![Screenshot 2024-01-03 060531](https://github.com/GSanthosh007/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147527586/1349a918-546f-48ce-9399-04bb1e73957d)

T FLIP FLOP:
![Screenshot 2024-01-03 060544](https://github.com/GSanthosh007/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147527586/403c0ea9-719c-4d27-b9da-d97b9a06a444)


TRUTH TABLE:
SR FLIP FLOP:
![Screenshot 2024-01-03 060618](https://github.com/GSanthosh007/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147527586/ebe7ae31-2405-413f-9c9b-b91733d36cb7)


D FLIP FLOP:
![Screenshot 2024-01-03 060635](https://github.com/GSanthosh007/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147527586/b013a054-0254-4967-a3d6-b8bd0feaab82)


JK FLIP FLOP:
![Screenshot 2024-01-03 060657](https://github.com/GSanthosh007/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147527586/2164d6df-7cae-4e29-a21a-3e1081c40362)


T FLIP FLOP:
![Screenshot 2024-01-03 060715](https://github.com/GSanthosh007/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147527586/2a9fc633-9283-4e2b-9bad-c47a0d2c48e0)



### TIMING DIGRAMS FOR FLIP FLOPS 

SR FLIP FLOP:
![Screenshot 2024-01-03 060741](https://github.com/GSanthosh007/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147527586/bcc7ce89-75c3-4689-b2d1-c2d8167ee601)


D FLIP FLOP:
![Screenshot 2024-01-03 060804](https://github.com/GSanthosh007/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147527586/885f696f-7e34-4de3-ab41-a5ef56fa7936)

JK FLIP FLOP:
![Screenshot 2024-01-03 060819](https://github.com/GSanthosh007/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147527586/9edf2fa9-d1e9-4442-b1b3-ffdbdbf3edf5)

T FLIP FLOP:
![Screenshot 2024-01-03 060913](https://github.com/GSanthosh007/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147527586/ca322cb8-ea8c-4288-b0b6-343dc73a58c3)

### RESULTS 
Thus, all the FLIP FLOPS are designed and the truth tables are verified using quartus software.
