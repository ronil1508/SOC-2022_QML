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

### Quantum Circuits
 A quantum circuit is to be read left to right. Each line in the circuit represents a wire in the quantum circuit. This wire does not necessarily correspond to a physical wire; it may correspond instead to the passage of time, or perhaps to a physical particle such as a photon – a particle of light – moving from one location to another through space. It is conventional to assume that the state input to the circuit is a computational basis state.
 The peculiar differences between classical and quantum circuits are :
 
 1) We don’t allow ‘loops’, that is, feedback from one part of the quantum circuit to another; we say the circuit is _acyclic_.
 2) Classical circuits allow wires to be ‘joined’ together, an operation known as FANIN, with the resulting single wire containing the bitwise of the inputs. This operation is not reversible and therefore not unitary, so we don’t allow FANIN in our quantum circuits.
 3) The inverse operation, , whereby several copies of a bit are produced is also not allowed in quantum circuits. In fact, it turns out that quantum mechanics forbids the copying of a qubit, making the operation impossible!
 
Two important elements of a quantum circuit are: 

1) Controlled Gates - The controlled U gate has one control qubit and n target qubits on which a n x n unitary matrix acts as an operator. </li> ![image](https://user-images.githubusercontent.com/95964330/164993180-7653680e-7c97-4d86-aac4-7ac4bb871858.png)
2) "Meter" for measurment of the quantum bit, the measurement of a qubit collapses it's state and gives classical bits 0  or 1 as the result. </li> ![image](https://user-images.githubusercontent.com/95964330/164993191-713ae328-4c33-45ce-8788-6b28ec4c8963.png)

### No Cloning Theorem
The no cloning theorem states that it is e impossible to make a copy of an unknown quantum state. Once one qubit is measured, the state of the other one is completely
determined, and no additional information can be gained. In this sense, the extra hidden information carried in the original qubit was lost in the first measurement, and cannot be regained. If, however, the qubit had been copied, then the state of the other qubit should still contain some of that hidden information. Therefore, a copy cannot have been created.

### Quantum Teleportation
Quantum teleportation is a technique for moving quantum states around, even in the absence of a quantum communications channel linking the sender of the quantum state to the recipient. It uses the fact that the qubits in the Bell state are strongly corelated with one another. We take help of our friends Alice and Bob to undertsand this concept.
Quantum teleportation works as follows:
1) Alice and Bob meet each other and generate an EPR pair. Both of them take one qubit from the EPR pair.
2) Alice sends her qubits through a CNOT gate then sends the unknown qubit through the H-gate. She measures her set of qubits and sends it to Bob.
3) Depending on Alice’s measurement outcome, Bob’s qubit will end up in one of the four possible states. In the case where the measurement yields 00, Bob doesn’t
need to do anything. If the measurement is 01 then Bob can fix up his state by applying the X gate. If the measurement is 10 then Bob can fix up his state by applying the Z gate. If the measurement is 11 then Bob can fix up his state by applying first an X and then a Z gate.

<img src="https://user-images.githubusercontent.com/95964330/167312994-c528ff60-0ba9-4331-bf52-91f373f8b6d2.png" width=40% height=40%>

In hindsight it seems that teleportation allows faster than light communications but this insight is incorrect. This is because Alice needs to transfer the results of her measurements through a classical communication channel. This limits the speed of information tranfer. Secondly, it appears that teleportation creates a copy of the qubit to be transferred violating the no-cloning theorem. This violation is only illusory since after the teleportation process only the target qubit is left in the original state, and the original data qubit ends up in one of the computational basis states.

### Quantum Algorithms
Any classical circuit can be replaced by an equivalent circuit containing only reversible elements, by making use of a reversible gate known as the Toffoli gate. The Toffoli gate has three input bits and three output bits. 

<img src="https://user-images.githubusercontent.com/95964330/167313676-adf4aafe-49c2-43c3-a2e3-36e4832b5646.png" width=40% height=40%>

Two of the bits are control bits that are unaffected by the action of the Toffoli gate. The third bit is a target bit that is flipped if both control bits are set to 1, and otherwise is left alone. Any classical circuit can be simulated using a Toffoli gate. 

_Quantum parallelism_ is a fundamental feature of many quantum algorithms. Heuristically, and at the risk of over-simplifying, quantum parallelism allows quantum computers to evaluate a function f(x) for many different values of x simultaneously. 

The following algorithms use quantum paralleism:

1)Deutsch’s algorithm:

Deutsch’s algorithm combines quantum parallelism with a property of quantum mechanics known as interference. The bried overview of steps that the algorithm follows is: 
We send the computational basis 0 and 1 through a H-gate. Then we pass the first qubit through a H gate again. The final measurement of the first qubit gives us the result f(0) XOR f(1) in a single step which would have taken twice as many steps in any classical circuit.

2)The Deutsch–Jozsa algorithm:

Deutsch’s algorithm is a simple case of a more general quantum algorithm, which we shall refer to as the Deutsch–Jozsa algorithm. The Deutsch–Jozsa algorithm is used to decide if an oracle is balanced or constant. Using quantum parallelism the algorithm gives the answer in a single step. Intutively, in a constant oracle the qubits in the query register and the qubit in the target regsiter don't interfere with each other and the state of the qubit in the query regsiter doesn't change giving probability 1 of the query register being in state |00000....> when measured. Similarly, in a balanced oracle the qubits in the query and target register interfere with one another giving the probability of the qubit in query register being in state |0000....> to be 0.

_The topics covered in the Linear Algebra part of week 1 were a recollection of the topics learnt in MA106 and for refernce can be seen from QCQI_

## Week 2 - A Deeper Dive into Quantum Circuits
### Quantum Algorithms
The spectacular promise of quantum computers is to enable new algorithms which render feasible problems requiring exorbitant resources for their solution on a classical computer. At the time of writing, two broad classes of quantum algorithms are known which fulfill this promise. The first class of algorithms is based upon Shor’s quantum Fourier transform, and includes remarkable algorithms for solving the factoring and discrete logarithm problems, providing a striking exponential speedup over the best known classical algorithms. The second class of algorithms is based upon Grover’s algorithm for performing quantum searching. These provide a less striking but still remarkable quadratic speedup over the best possible classical algorithms.

### Single qubit operations
The Pauli matrices give rise to three useful classes of unitary matrices when they are exponentiated, the rotation operators about the x, y, and z axes, deﬁned by the equations:

<img src="https://user-images.githubusercontent.com/95964330/168089904-6daf598e-789b-4c68-8dd3-eada894cc927.png" width=40% height=40%>

An arbitrary unitary operator on a single qubit can be written in many ways as a combination of rotations, together with global phase shifts on the qubit. The following theorem provides a means of expressing an arbitrary single qubit rotation that will be particularly useful in later applications to controlled operations.

#### Z-Y decomposition for a single qubit: 
Suppose U is a unitary operation on a single qubit. Then there exist real numbers α, β, γ and δ such that

<img src="https://user-images.githubusercontent.com/95964330/168090687-ebd36686-c3d8-43fa-ae30-5b87a791c982.png" width=23% height=23%>

Suppose U is a unitary gate on a single qubit. Then there exist unitary operators A, B, C on a single qubit such that ABC = I and 
<img src="https://user-images.githubusercontent.com/95964330/168091337-4c154f70-6539-482c-985e-71a7db28b839.png" width=17% height=17%>
where α is some overall phase factor.

### Controlled operations
'If A is true, then do B’. This type of _controlled_ operation is one of the most useful in computing, both classical and quantum. The prototypical controlled operation is the controlled- NOT. CNOT is a quantum gate with two input qubits, known as the control qubit and target qubit, respectively.  In terms of the computational basis, the action of the CNOT is given by |c>|t>→|c>|t ⊕ c>; that is, if the control qubit is set to |1> then thetarget qubit is flipped, otherwise the target qubit is left alone.

More generally, suppose U is an arbitrary single qubit unitary operation. A controlled U operation is a two qubit operation, again with a control and a target qubit. If the control qubit is set then U is applied to the target qubit, otherwise the target qubit is left alone; that is, |c>|t>→|c>U|t>.

<img src="https://user-images.githubusercontent.com/95964330/168092291-f44fe741-8790-47f5-8006-9c175c9a5178.png" width=20% height=20%>

Unlike ideal classical gates, ideal quantum gates do not have (as electrical engineers say) ‘high-impedance’ inputs. In fact, the role of ‘control’ and ‘target’ are arbitrary – they depend on what basis you think of a device as operating in. We have described how the behaves with respect to the computational basis, and in this description the state of the control qubit is not changed. However, if we work in a different basis then the control qubit does change: its phase is flipped depending on the state of the ‘target’ qubit! 
The controlled U operation can be performed for arbitrary single qubit U, using only single qubit operations and the CNOT gate. The strategy is a two-part procedure based upon the decomposition <img src="https://user-images.githubusercontent.com/95964330/168091337-4c154f70-6539-482c-985e-71a7db28b839.png" width=17% height=17%>
