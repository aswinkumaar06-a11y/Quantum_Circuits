# Quantum_Circuits

⚛️Welcome to my Quantum Circuits repository! This is a collection of fundamental quantum computing programs designed to explore the mechanics of qubits, gates, and entanglement.Whether you're just starting with Qiskit or looking for a reference for standard gates, this repo serves as a "Hello World" for the quantum realm.

🚀 Getting StartedMost of the circuits in this repository are built using Qiskit (Python). To run these locally, you'll need to set up your environment:
Install Qiskit:

Bashpip install qiskit qiskit-aer matplotlib

Clone the Repo:

Bashgit clone https://github.com/your-username/quantum-circuits.git
cd quantum-circuits

📂 Featured Circuits

Circuit Name                  Description                                                Key Gates Used
Superposition             Creating a 50/50 chance of measuring 0 or 1.                   H (Hadamard)
Bell State                The classic "spooky action at a distance" (Entanglement).      H, CX (CNOT)
Quantum Teleportation     Transferring quantum states between qubits.                    H, CX, Barrier
Bernstein-Vazirani        A speedup algorithm to find a hidden bitstring.                H, X, CX

🛠 Example Code: The Bell StateThe following snippet creates a simple entangled state where measuring one qubit immediately tells you the state of the second.
Python:

from qiskit import QuantumCircuit
from qiskit_aer import AerSimulator

# 1. Initialize a 2-qubit circuit
qc = QuantumCircuit(2)

# 2. Add gates to create entanglement
qc.h(0)          # Put qubit 0 into superposition
qc.cx(0, 1)      # Entangle qubit 1 with qubit 0

# 3. Measure the results
qc.measure_all()

# 4. Simulate
simulator = AerSimulator()
result = simulator.run(qc).result()
counts = result.get_counts()

print(f"Measurement Results: {counts}")


📊 Visualizing Results

Quantum computing is as much about the math as it is the visualization. Most scripts in this repo include logic to generate:
Circuit Diagrams: To see the gate sequence.
Histograms: To visualize probability distributions of the measurement outcomes.
Bloch Spheres: To track the state of a single qubit in 3D space.

📜 License
This project is open-source under the MIT License. Feel free to fork, experiment, and break things!


Note: These circuits are optimized for simulators. If you plan to run these on actual IBM Quantum hardware, ensure you have your IBMQ API token configured.
