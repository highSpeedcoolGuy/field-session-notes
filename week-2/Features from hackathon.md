

Here are the features that other teams extracted:


> "file,backend,precision,n_lines,n_nonempty_lines,n_qubits,n_qreg_declarations,n_classical_bits,n_measure,n_barrier,n_cx,n_cz,n_cp,n_cy,n_ch,n_swap,n_ccx,n_csw      ap,n_2q_gates,n_3q_gates,n_x,n_y,n_z,n_h,n_s,n_sdg,n_t,n_tdg,n_rx,n_ry,n_rz,n_u1,n_u2,n_u3,n_u,n_1q_gates,n_total_gates,n_unique_edges,n_edge_repetitions,max      _qubit_degree,avg_qubit_degree,qubit_degree_std,n_connected_components,crude_depth,gates_per_layer_estimate,avg_gate_span,max_gate_span,std_gate_span,entangl      ement_pressure,midpoint_cut_crossings,has_qft_pattern,n_qft_like_gates,has_iqft_pattern,has_grover_pattern,has_variational_pattern,n_rotation_gates,has_ghz_p      attern,n_custom_gates,n_opaque_gates,ratio_2q_gates,ratio_1q_gates,gates_per_qubit,2q_gates_per_qubit,1q_gates_per_qubit,circuit_density,max_fidelity_achieve      d,forward_shots,forward_peak_rss_mb,n_thresholds_tested,min_threshold,forward_runtime "


If you wanted to design a quantum circuit that explicitly exploits the weaknesses of a classical simulator to maximize processing time without simply maximizing the qubit count, what structural features or patterns would you use?


Gates take longer 

Efficiencies - 
Determine Tensor networks - classical speedup of quantum simulations

Number of gates - 

Each gate is a matrix - 
QASM files - gates applied to qubits
cx


Understanding their simulations will help us determine how compute increments
- Identify slow and fast parts of simulators

Detect if speedup techniques are used? (i.e. Gate cuts)

Post extraction data manipulation

Virtual registration

Qir, Quake, OpenQASm (Simplest)

Counting number of gates (different runtimes for gates)
t-gates are slowed down in classical simulation
code depth - DAG to measure depth
QASM -> DAG for optimization (ML)
Shots - needs multiple for variation to be more accurate
		- Difference in means for shots and hardware (blocking technique)
Random circuits with no structure
Look at other qiskit codes and turn them into qasm.

Questions for client:
Simulation speedup/optimizaiton techniques
	- Some methods are non-deterministic (NP-hard)
Baseline Runtimes of specific gates
How qubits are stored, and how are they applied (identify potential causes of slowdown)
What use-cases are they're trying to fit? (Maybe this may be more general)
New techniques may be released due to research (scalable)
Are noise reduction techniques used, if not may need a lot of shots/runs?
