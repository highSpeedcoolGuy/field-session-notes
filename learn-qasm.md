O
# Definitions

#### Superposition 
> A superposition is ...

#### Entanglement 
> ...

#### Gates


#### Hilbert's Space


#### Measurement



``` |0> ```



qreg - quantum registers
creg - classical registers
h - Hadamard gate
cx - control not gate 
measure - 



![[Pasted image 20260520233506.png]]

Now translating this into QASM:

``` qc = QuantumCircuit(2, 2) ``` means that we need 2 quantum bits, and 2 classical bits.
Thus: 
```qreg [2];``` 
```creg [2];```

Moving on to ```qc.h(0)```
This translates into a Hadamard gate that is a 0:
```h q[0];``` 

Then: ```qc.cx(0,1)```
```cx q[0], q[1];```

and finally, ```qc.measure_all()```
```
measure q[0] -> c[0];
measure q[1] -> c[1];

```

So:
```{qasm}

qreg[2];
creg[2];
h q[0];
cx q[0], q[1];
measure q[0] -> c[0];
measure q[1] -> c[1];
```

This program has either of two results:


| Chance | Classical Bit | Quantum Bit |
| ------ | ------------- | ----------- |
|   50%  |      0        |      0      |
|   50%  |      1        |      1      |

This is due to the operation of a controlled not gate ``cx`` working immediately after the creation of a hadamard gate. The Hadamard gate ``h`` defines our quantum bit. And that bit can now either be 0 or 1. 












## Helpful Materials to Learn These basics:
### Videos
[Quantum Instruction Set - Computerphile](https://www.youtube.com/watch?v=ZN0lhYU1f5Q&t=293s)
[What is Quantum Computing - IBM](https://www.youtube.com/watch?v=lt4OsgmUTGI)
["But what is quantum computing?" - 3B1B](https://www.youtube.com/watch?v=RQWpF2Gb-gU&t=13s)

### Sites
[MATH3MA](https://www.math3ma.com/) - for general basic knowledge of low level quantum operations
[Visualizing Quantum Circuits using python - IBM](https://quantum.cloud.ibm.com/docs/en/guides/visualize-circuits)
