## 5_PARITY_GENERATOR
Implementation of 5 bit parity generator

## AIM:
To implement the given logic function and to verify its operation in Quartus using Verilog programming

## EQUIPMENT REQUIRED:
Hardware-PCs,Cyclone ||,USB flasher
Software-Quartus prime
## INTRODUCTION:
A parity generator is a digital circuit that generates a parity bit, which is a bit added to a group of bits to ensure that the number of 1s in the group is even (or odd). A 5-bit parity generator generates a parity bit for a group of 5 bits. The parity bit is added to the group of 5 bits to form a 6-bit code, with the purpose of detecting errors in data transmission or storage. If the number of 1s in the original 5 bits is even, the parity bit is set to 0. If the number of 1s in the original 5 bits is odd, the parity bit is set to 1. This way, when the 6-bit code is received or read, a simple parity check can be performed to detect any errors that may have occurred during transmission or storage.
## LOGIC DIAGRAM:
A logic diagram is a graphical representation of a digital circuit, showing the logical connections between the circuit components. In the case of a 5-bit parity generator, the logic diagram would show the input pins for the 5-bit data and the output pin for the parity bit, as well as the digital gates used to generate the parity bit from the input data.
The basic structure of a 5-bit parity generator logic diagram would include:

Five input pins, one for each bit of the 5-bit data.

One output pin for the parity bit.

A series of AND gates, one for each input bit. The AND gates are used to determine the number of 1s in the input data.

An OR gate, which receives the output of the AND gates as input. The OR gate generates the sum of all the input.

An XOR gate, which receives the output of the OR gate as input. The XOR gate compares the output of the OR gate with the constant value of 1.

The output of the XOR gate is the parity bit.

It is important to note that the above-described logic diagram is a basic implementation, and different designs may have variations depending on the specific requirements and constraints.
##  PROCEDURE:
1. Design an even/odd parity generator for 5-bit data.
2. Design a parity checker circuit for a 5-bit data.
3. Design a logic circuit for a 4-bit message to be transmitted with an even parity bit.
4. Five data bits are to be transmitted. Design a parity bit generator to give an o/p of '1' if the
number of logic 1's in the message is: (i) odd; (ii) even.
## PROGRAM:
```
module pg5bit(a,b,c,d,e,y);
input a,b,c,d,e;
output y;
wire l,m,n;
xor(l,a,b);
xor(m,c,d);
xor(n,m,e);
xor(y,l,n);
endmodule
```
## RTL Realization:
![5 bit pg RTL](https://user-images.githubusercontent.com/121418522/213696675-1ad958b0-92d5-4084-a137-69b0861b2025.png)

## TRUTH TABLE:
![5 bit truthtable](https://user-images.githubusercontent.com/121418522/213696779-4da17cd0-0a72-419f-8957-bd1cd786c878.png)

## TIMING DIAGRAM:
![5 bit pg timing](https://user-images.githubusercontent.com/121418522/213696897-5b22f0bc-619a-4e39-8641-f3429eb3b35d.png)

## RESULT:
 thus the  given logic function are implemented using XOR gate and their operations are verified using Verilog programming







