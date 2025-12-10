# CFD Simulation: Coaxial Stream in a Square Tube using k-epsilon Model

## Overview

This project contains an OpenFOAM simulation of a coaxial stream flowing through a square tube using the k-epsilon turbulence model.

## Simulation Setup

### Geometry and Flow Conditions
- **Tube dimensions**: 0.1m × 0.1m × 1m square tube
- **Inner stream**: 
  - Velocity: 1 m/s
  - Radius: 0.02m
- **Outer stream**: 
  - Velocity: 5 m/s
- **Fluid properties**: 
  - Kinematic viscosity: 1.5×10⁻⁵ m²/s (air)

### Numerical Setup
- **Solver**: `simpleFoam` (steady-state, incompressible)
- **Turbulence modeling**: k-epsilon RANS model (enabled)
- **Simulation type**: Steady-state

### Computational Mesh
- **Resolution**: 40 × 40 × 200 cells
- **Total cells**: 320,000
- **Mesh type**: Structured hexahedral
- **Boundary conditions**: No-slip walls, pressure outlet

## Results and Visualization

The simulation produced comprehensive results showing the coaxial flow characteristics. Key visualizations are included below:



### Velocity Field
<div style="display: flex;">
  <img src="squareTube/screenshots/velocity%20slice%20along%20tube.png" alt="Velocity Slice" width="49%">
</div>
*Velocity magnitude along the tube length*



### Pressure Distribution
<div style="display: flex;">
  <img src="squareTube/screenshots/pressure%20slice%20along%20tube.png" alt="Pressure Slice" width="49%">
</div>
*Pressure distribution along the tube*

### Turbulence Characteristics
<div style="display: flex;">
  <img src="squareTube/screenshots/turbulent%20energy%20slice%20along%20tube.png" alt="Turbulent Energy" width="49%">
  <!-- Add another image here if you want a pair -->
</div>

*Turbulent kinetic energy (k) distribution*




## Usage

To run or analyze this simulation:

1. Navigate to the `squareTube/` directory
2. Use OpenFOAM commands:
   - `blockMesh` to generate/review the mesh
   - `simpleFoam` to run the steady-state simulation
   - `paraFoam` to visualize results
   - `foamToVTK` to convert results for external visualization

## Key Findings

- Successful simulation of coaxial flow in square tube geometry
- Proper development of velocity profiles along the tube length
- Expected pressure drop characteristics
- Realistic turbulence distribution with higher k near inlet and walls
- Stable convergence with k-epsilon model
- Results consistent with fluid dynamics principles for internal flows

## Notes

- This simulation serves as the primary/reference case
- A comparative RSM simulation is available in `squareTube_RSM/` for validation
- All visualizations were created using ParaView
- Simulation demonstrates proper handling of coaxial flow with turbulence modeling

## License

This is an academic CFD project created for educational purposes at JKU.# coaxial-stream-simulation
