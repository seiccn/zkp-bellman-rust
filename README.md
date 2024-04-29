
# Zero Knowledge Proof (ZKP) Demonstration in Rust

This project is a Rust-based demonstration of a simple Zero-Knowledge Proof (ZKP) system. It illustrates how a prover can convince a verifier that they know a secret without revealing the secret itself.

## Introduction to Bellman

Bellman Zero-Knowledge Proofs (ZKPs) are cryptographic protocols that allow one party, the prover, to convince another party, the verifier, that a certain statement is true without revealing any additional information beyond the validity of the statement itself. The term "Bellman" in Bellman ZKPs refers to the use of the Bellman-Ford algorithm, a classic algorithm in graph theory, adapted for zero-knowledge proof purposes.

## How to Build and Run

Make sure you have Rust installed on your system. If not, you can install it using [rustup](https://rustup.rs/).

To execute the project, navigate to its directory in your terminal and enter the following command:

```
cargo run
```

## Implementation Details

In this example, we define a simple circuit that enforces the constraint `a * b = c`, where `a`, `b`, and `c` are inputs. We then generate random values for `a` and `b`, compute the expected value of `c`, and use these values to create an instance of the circuit.

We then generate a proving key and a verification key using the `generate_random_parameters` function, which takes the circuit instance and a random number generator as inputs. We use these keys to create a proof of correctness using the `create_random_proof` function, and then verify the proof using the `verify_proof` function and the verification key.

Note that this is just a simple example to illustrate the basic concepts of ZKPs in Rust using the Bellman library. In practice, ZKPs can be much more complex, and the implementation details will depend on the specific use case.
