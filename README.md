# SoC-2022_QML
An introduction to QC, ML and QML

## Week 1 - Introduction to QC
### What is a Qubit?
Just as a classical bit has a state either 0 or 1 a qubit also has a state. The possible states for a qubit are  <img src="https://user-images.githubusercontent.com/95964330/164874781-7c8f5ff1-5a00-496c-8f3c-0c8a34f5fea6.png" width=2.2% height=2.2%> and <img src="https://user-images.githubusercontent.com/95964330/164912039-69f001dd-55f6-45e6-9c87-9f276af6081b.png" width=2.2% height=2.2%> . The states <img src="https://user-images.githubusercontent.com/95964330/164874781-7c8f5ff1-5a00-496c-8f3c-0c8a34f5fea6.png" width=2.2% height=2.2%> and <img src="https://user-images.githubusercontent.com/95964330/164912039-69f001dd-55f6-45e6-9c87-9f276af6081b.png" width=2.2% height=2.2%> are known as the computational basis state and unlike a classical bit a qubit can be in the superposition of these states. 
The general state of a qubit can be represented by <img src="https://user-images.githubusercontent.com/95964330/164874629-662d2bef-87f2-4040-998a-5c9d68ef021c.png" width=20% height=20%> where alpha and beta are complex numbers and the state of the qubit is a vector of norm 1. We cannot observe and state of a qubit and this dichotomy between the unobservable state of a qubit and the observations we can make lies at the heart of quantum computation and quantum information. 
### Bloch sphere representation
In spherical co-ordinates the general state of a qubit can be written as ![Linear combination](https://user-images.githubusercontent.com/95964330/164911312-21d86906-97e0-4f2c-af14-f1f528ef83e5.png)
and can be represented on a sphere as shown on a Bloch Sphere:
<img src="https://user-images.githubusercontent.com/95964330/164911401-18eaa4fc-23b2-4623-a6f0-2630dfee2f4b.png" width=20% height=20%>

How much information is represented by a qubit? Paradoxically, there are an infinite number of points on the unit sphere, so that in principle one could store an entire text of Shakespeare in the infinite binary expansion. However this turns out to be misleading as when we measure the state of a qubit we only get _0_ or _1_ as the measurements collapsing the state of the qubit. 

### Multiple Qubits
Suppose we have two qubits. If these were two classical bits, then there would be four possible states, 00, 01, 10, and 11. Correspondingly, a two qubit system has four
computational basis state denoted by <img src="https://user-images.githubusercontent.com/95964330/164911803-8a1d0b81-915b-4169-8777-876bcc9f42c2.png" width=10% height=10%>. A pair of qubits can also exist in superpositions of these four states, so the quantum state of two qubits involves associating a complex coefficient – sometimes called an _amplitude_ – with each computational basis state.
An important two qubit state is the Bell state or EPR pair,

<img src="https://user-images.githubusercontent.com/95964330/164911760-a353c3dd-6938-45c4-bf37-53ed46193dc2.png" width=10% height=10%>

The Bell state has a property that upon measurement both it's qubits are always in the same state. That is, the measurement outcomes are _correlated_. EPR’s insights were taken up and greatly improved by John Bell, who proved an amazing result: the measurement correlations in the Bell state are stronger than could ever exist between classical systems

### Quantum Computation
As in the case of classical computer the changes occuring in quantum circuits can be described using quantum computation using quantum circuits which are built of wires to carry the information around and _quantum gates_ to manipulate the information.
#### Single Qubit gates
Any unitary operator can act as a single qubit gate. This is because quantum gates have to be norm preserving so that the sum of individual probabilities does not exceed 1 and also quantum gates needs to be reversible. Both these properties are satisfied by unitary matrices. It can be further proved that unitarty matrices are the only class of matrices which satisfy both these requirements. The operation of a single qubit gate on a qubit can be thought as the rotation of the qubit around the Bloch sphere. 
All the single qubit gates act linearly. Non-linear behaviour of operators can lead to paradoxes such as - time travel, faster-than-light-communication etc.

The important single qubit gates are:

1) The quantum NOT gate (X gate) - 

![image](https://user-images.githubusercontent.com/95964330/164912638-f70b94a5-414b-4187-96b6-d88363e70f34.png).

It's operation can be seen as ![image](https://user-images.githubusercontent.com/95964330/164912741-f88a8066-09cb-4ca6-8a89-b787ed49870a.png)

2) The Z gate -

![image](https://user-images.githubusercontent.com/95964330/164912658-67ff1906-9302-4fd0-ad4c-58e36efc1059.png)

3) The Hadamard gate - 

![image](https://user-images.githubusercontent.com/95964330/164912666-d40c7ca7-e7fb-4559-aff2-acf71fea4742.png)

The Hadamard gate is one of the most useful quantum gates, and it's operation can be visualized by considering the Bloch sphere picture. The Hadamard operation is just a rotation of the sphere about the y axis by 90◦, followed by a rotation about the x axis by 180◦
The action of these important single qubit gates can be summarised as:

<img src="https://user-images.githubusercontent.com/95964330/164912718-87d63d1e-2115-46ff-a5f8-9ea860a76961.png" width=50% height=50%>

Any set of single-quibit gates can be constructed out of a _finite- set of qantum gates - not always exactly, but to an _arbitrarily_ good precision; using the decomposition: 

<img src="https://user-images.githubusercontent.com/95964330/164959380-c167ae2f-2cee-4b39-8015-1c7001f01f0d.png" width=50% height=50%>

### Multiple Qubit Gates
The prototypical multi-qubit logic gate is the _controlled_-NOT or _CNOT_ gate - the first quibt decides whether the second qubit will be flipped or not. the second qubit will be flipped only if the first qubit (_control qubit_) is set to 1. The action of the gate can be summarised as: <img src="https://user-images.githubusercontent.com/95964330/164959586-e00f0c75-dce5-424c-9b68-d32a7f76a524.png" width=15% height=15%>,it is a generalization of the classical XOR gate and can be represented by the matrix:

<img src="https://user-images.githubusercontent.com/95964330/164959626-410d1480-5b14-4615-8e48-73e5d12a72ed.png" width=15% height=15%>

There are many interesting quantum gates other than the controlled- NOT .However, in a sense the controlled- and single qubit gates are the prototypes for all other gates because of the following remarkable universality result: Any multiple qubit logic gate may be composed from and single qubit gates.

### Measurements in bases other than the computational basis
It is not necessary to use the computational bases as the basis for our measurement. Any set of orthonormal vectors can be used as the basis. 
It is possible in principle to measure a quantum system of many qubits with respect to an arbitrary orthonormal basis. However, just because it is possible in principle does not mean that such a measurement can be done easily. 
