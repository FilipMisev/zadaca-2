# zadaca-2
To initialize the 8155/56 component so that the RAM occupies space 4800h–48FFh. Port A to be initialized as a gated input port, and B as a normal output port. The timer counts a train of short pulses with T = 1ms. (f=4MHZ).

 ![Screenshot (1)](https://github.com/FilipMisev/zadaca-2/blob/main/2.png)


CSR 01001 000
PA 01001 001
PB 01001 010
PC 01001 011
TLSB 01001 100
TMSB 01001 101 
TMSB 11000111
TLSB 11010000
CSR 11010110
MVI A, 208d CSR EQV 01001000
OUT TLSB TMSB EQV 01001101
MVI A, 199d TLSB EQV 01001100
OUT TMSB
MVI A, D6h
OUT CSR
END 

