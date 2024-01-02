# Exp-6-Synchornous-counters - up counter and down counter 
### AIM: 
To implement 4 bit up and down counters and validate  functionality.
### HARDWARE REQUIRED:  – PC, Cyclone II , USB flasher
### SOFTWARE REQUIRED:   Quartus prime
## THEORY 

## UP COUNTER 
The counter is a digital sequential circuit and here it is a 4 bit counter, which simply means it can count from 0 to 15 and vice versa based upon the direction of counting (up/down). 

The counter (“count“) value will be evaluated at every positive (rising) edge of the clock (“clk“) cycle.
The Counter will be set to Zero when “reset” input is at logic high.
The counter will be loaded with “data” input when the “load” signal is at logic high. Otherwise, it will count up or down.
The counter will count up when the “up_down” signal is logic high, otherwise count down

Since we know that binary count sequences follow a pattern of octave (factor of 2) frequency division, and that J-K flip-flop multivibrators set up for the “toggle” mode are capable of performing this type of frequency division, we can envision a circuit made up of several J-K flip-flops, cascaded to produce four bits of output.
The main problem facing us is to determine how to connect these flip-flops together so that they toggle at the right times to produce the proper binary sequence.
Examine the following binary count sequence, paying attention to patterns preceding the “toggling” of a bit between 0 and 1:
Binary count sequence, paying attention to patterns preceding the “toggling” of a bit between 0 and 1.

Note that each bit in this four-bit sequence toggles when the bit before it (the bit having a lesser significance, or place-weight), toggles in a particular direction: from 1 to 0.



 
 

Starting with four J-K flip-flops connected in such a way to always be in the “toggle” mode, we need to determine how to connect the clock inputs in such a way so that each succeeding bit toggles when the bit before it transitions from 1 to 0.

The Q outputs of each flip-flop will serve as the respective binary bits of the final, four-bit count:

 
 

Four-bit “Up” Counter
![image](https://user-images.githubusercontent.com/36288975/169644758-b2f4339d-9532-40c5-af40-8f4f8c942e2c.png)



## DOWN COUNTER 

As well as counting “up” from zero and increasing or incrementing to some preset value, it is sometimes necessary to count “down” from a predetermined value to zero allowing us to produce an output that activates when the zero count or some other pre-set value is reached.

This type of counter is normally referred to as a Down Counter, (CTD). In a binary or BCD down counter, the count decreases by one for each external clock pulse from some preset value. Special dual purpose IC’s such as the TTL 74LS193 or CMOS CD4510 are 4-bit binary Up or Down counters which have an additional input pin to select either the up or down count mode.
![image](https://user-images.githubusercontent.com/36288975/169644844-1a14e123-7228-4ed8-81a9-eb937dff4ac8.png)


4-bit Count Down Counter
### Procedure

1.Create a new project in Quartus II software. 
2.Name the project as uc for upcounter and dc for downcounter.
3.Create a new Verilog HDL file in the project file. 
4.Name the module as dc and uc for downcounter and upcounter. 
5.Within the module declare input and output variables. 
6.Complete the program. 
7.End the module.


## PROGRAM 

## UP COUNTER 
![image](https://github.com/KAMALESHNITHYA/Exp-7-Synchornous-counters-/assets/145743119/f3bd9e8a-3aef-4c77-8688-25ae58683cdf)

## DOWN COUNTER 
![image](https://github.com/KAMALESHNITHYA/Exp-7-Synchornous-counters-/assets/145743119/c9312eff-6752-48ba-8dd0-501211682e08)


## RTL LOGIC UP COUNTER AND DOWN COUNTER  

## UP COUNTER
![image](https://github.com/KAMALESHNITHYA/Exp-7-Synchornous-counters-/assets/145743119/fc59ef2d-6945-4e83-82c4-9fcc91503c2c)


## DOWN COUNTER
![image](https://github.com/KAMALESHNITHYA/Exp-7-Synchornous-counters-/assets/145743119/f2080a4a-2293-46f9-a5e6-cedd5776ea3d)




## TIMING DIGRAMS FOR COUNTER  

## UP COUNTER
![image](https://github.com/KAMALESHNITHYA/Exp-7-Synchornous-counters-/assets/145743119/57a20d5b-41fd-4aae-9d11-3790d834a5ef)


## DOWN COUNTER
![image](https://github.com/KAMALESHNITHYA/Exp-7-Synchornous-counters-/assets/145743119/4c95c28a-74eb-4d40-b32c-83782a6cc6d5)


## STATE TABLE 

## UP COUNTER
![image](https://github.com/KAMALESHNITHYA/Exp-7-Synchornous-counters-/assets/145743119/eff116b4-f139-479b-95df-834c497e42c4)


## DOWN COUNTER
![image](https://github.com/KAMALESHNITHYA/Exp-7-Synchornous-counters-/assets/145743119/3593ab95-26e4-47e8-9eb6-39eec56bed42)


## RESULTS 
Thus we have verified the truthtable of 4-bit up and down counter using verilog.
