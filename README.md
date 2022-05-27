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
 https://![image](https://user-images.githubusercontent.com/103634390/170633366-000036f3-8aff-4f0a-a98f-7f3b43c7212b.png)

