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
![Screenshot 2024-01-03 054603](https://github.com/GSanthosh007/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147527586/cf9c8c69-fe0d-42de-8817-b30cc1aaca50)



### PROGRAM 
/*
Program for flipflops  and verify its truth table in quartus using Verilog programming.
Developed by: SANTHOSH G
RegisterNumber:212223240152  
*/
1.SR FLIP FLOP:
![Screenshot 2024-01-03 054803](https://github.com/GSanthosh007/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147527586/6930e308-9c35-4c03-a063-9749baaa5a75)

2.D FLIP FLOP:
![293019784-dc8ff246-1724-4728-b5a8-23b1ba044f4f](https://github.com/GSanthosh007/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147527586/9a0efe1a-864d-45ba-a91c-fc09b3e542c5)

3.JK FLIP FLOP:
![292614271-3a2c6afe-11ad-4c9a-bc05-a36a17c8aae3](https://github.com/GSanthosh007/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147527586/528a7ec1-3c08-4123-9072-93ce2dc61b32)

4.T FLIP FLOP:
![292614315-7caf3430-2a03-41c4-9b63-f40a96762e8f](https://github.com/GSanthosh007/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147527586/e71f1e49-57cf-469a-97bf-458134e29be5)

### RTL DIAGRAM:
SR FLIP FLOP:
![293020298-b63f61a5-2999-4ffd-94dc-eb8845d32a88](https://github.com/GSanthosh007/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147527586/30a4c063-03ca-47ae-8abb-be5a5074611f)

D FLIP FLOP:
![292614452-428b9ef2-e40d-4d48-abfe-8deb697f0716](https://github.com/GSanthosh007/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147527586/e54b4332-d2ef-49c5-b86f-fce2ba702634)

JK FLIP FLOP:
![292614459-528e49ea-929e-494a-a9b5-15ad8683bfaf](https://github.com/GSanthosh007/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147527586/cbdb2620-aac5-413e-a0fe-8bf05ab5fbbf)

T FLIP FLOP:
![292614465-1e241661-059b-4c49-b5aa-5370b1332633](https://github.com/GSanthosh007/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147527586/64a2b144-0d0b-4ffb-82a3-5663a6d72373)

TRUTH TABLE:
SR FLIP FLOP:
![292614705-d9a747b0-64b8-459d-85b1-94490db192bd](https://github.com/GSanthosh007/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147527586/77c964cd-94b2-4ba9-8152-2b35b8a5b000)


D FLIP FLOP:
![292614715-4340fbea-cddf-47a4-bb55-f2ab8dfc70ba](https://github.com/GSanthosh007/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147527586/098fb761-85cb-494e-8a4e-ce9177c08882)

JK FLIP FLOP:
![292614697-6b90369b-4af7-4534-b3f2-f867f1508eee](https://github.com/GSanthosh007/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147527586/96f6c15e-af0f-4ec8-bd90-7c63a92350cc)

T FLIP FLOP:
![292614717-82891beb-b60b-4680-8c9a-f41bce517a35](https://github.com/GSanthosh007/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147527586/e0ab393c-7b75-4333-bc99-0beb45a25b7a)


### TIMING DIGRAMS FOR FLIP FLOPS 

SR FLIP FLOP:
![293020388-4de8571c-1f75-4d57-b55f-b8b5984e24c9](https://github.com/GSanthosh007/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147527586/14c48601-b4cb-43a7-876c-1574126ee46b)

D FLIP FLOP:
![292614885-22173ffb-e3c5-423c-bc43-a40fe0c1875c](https://github.com/GSanthosh007/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147527586/c1695b1b-3bce-44a2-9f38-cd1934028205)

JK FLIP FLOP:
![292614891-ca771aa6-d3de-4e98-9371-631dc0db53b5](https://github.com/GSanthosh007/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147527586/7099a8f2-eb49-4c72-8174-2a2ff00acb65)

T FLIP FLOP:
![292614896-87a91196-6a87-4c89-ace5-5b3b624bc6fd](https://github.com/GSanthosh007/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147527586/39d2e9e3-d892-4a7a-9486-1397ae79f622)
### RESULTS 
Thus, all the FLIP FLOPS are designed and the truth tables are verified using quartus software.
