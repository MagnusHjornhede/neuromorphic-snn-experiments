# Simulating a Spiking Neural Network on DYNAP

This project explores how a Spiking Neural Network (SNN) can be simulated and prepared for execution on DYNAP neuromorphic hardware.

The implementation is provided in:

Simulating_an_SNN_on_DYNAP.ipynb



## Project Goal

Neuromorphic hardware such as DYNAP implements spiking neurons directly in silicon.  
Unlike conventional GPUs, these systems compute using asynchronous spike events and analog neuron dynamics.

This project investigates how to:

- Design a spiking neural network
- Simulate its temporal dynamics
- Map neuron and synapse parameters to DYNAP-compatible configurations
- Analyze how hardware-style constraints affect network behavior

For broader context:
- Neuromorphic computing overview (Nature): https://www.nature.com/articles/s41586-019-1677-2
- Surrogate gradient learning for SNNs: https://arxiv.org/abs/1901.09948



## What is DYNAP?

DYNAP is a mixed-signal neuromorphic processor designed for low-power, event-driven computation.

Unlike purely digital accelerators, it combines:

- Analog neuron and synapse circuits
- Event-driven spike communication
- Leaky Integrate-and-Fire (LIF) dynamics implemented in hardware

Official site:
- SynSense (DYNAP developer): https://www.synsense.ai/

These systems are optimized for processing temporal and event-based data efficiently.



## Network Architecture

The simulated network includes:

- Input spike streams
- Leaky Integrate-and-Fire neurons
- Configurable synaptic weights
- Adjustable threshold and leak parameters

Neuron behavior follows standard LIF dynamics:

- Membrane potential integrates incoming spikes
- When the threshold is reached, a spike is emitted
- The membrane potential resets

If unfamiliar with the LIF model:
- https://en.wikipedia.org/wiki/Leaky_integrate-and-fire

The notebook simulates these dynamics and evaluates resulting spike activity and stability.



## What This Project Demonstrates

- How SNN dynamics behave under hardware-style constraints
- How neuron parameters influence spike timing and firing rate
- How network configuration affects stability and activity patterns
- The practical gap between software SNN models and neuromorphic hardware implementations



## Why This Matters

Neuromorphic systems aim to:

- Reduce energy consumption
- Enable real-time event-driven processing
- Support edge AI applications
- Move toward biologically inspired computing architectures

Understanding simulation and parameter mapping is a critical step before deploying networks to physical neuromorphic hardware.



## Requirements

- Python ≥ 3.9
- NumPy
- Matplotlib
- (Optional) snnTorch or related spiking libraries

Install basic dependencies:

pip install numpy matplotlib



## Running the Project

Launch Jupyter:

jupyter notebook Simulating_an_SNN_on_DYNAP.ipynb

Run all cells sequentially.



This repository serves as a compact, hardware-aware exploration of spiking neural network dynamics and neuromorphic system design.
