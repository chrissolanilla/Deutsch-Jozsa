# Deutsch Jozsa Alorithm
This is a notebook that showcases the Deutsch-Jozsa Algorithm.

The algorithm is used to test if a function is constant or balanced.

We can use the notebook to simulate a quantum computer and how it would behave

## Terms
### The Oracle
An oracle seems to be a magic 8 ball that just knows the answer to everything in the universe.

In our case, an oracle is a function that takes a bit string as input and returns a bit as output.

### balanced vs constant function
A balanced function is one where, over all possible input bit strings, exactly half of them produce an output of 0 and the other half produce an output of 1.

A constant function is either its all 1's or 0's for a bit string.


# Why the quantum computer does it better than regular computers
In classical computing, you wold need to check more than half of all possible inputs for some function to know if its constant or balanced

That is O(2^n)


In quantum computing, you only need to do one call to this magical oracle.

That is O(1)


# How the algorithm works
You can read about the steps on [wikipedia](https://en.wikipedia.org/wiki/Deutsch%E2%80%93Jozsa_algorithm)

basically if you start with \ket{0}, then you want to make it \ket{1} by applying an X gate.
Then you apply an Hadamard Gate to give it super position.
Then you query the oracle, it already knows the answer
After you finish the query, then you apply another Hadamard gate to reveal if constant or balanced.

In python code with qiskit(IBM) library, you can see it defined in `def dj_algorithm()`


