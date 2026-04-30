# Design Optimisation and Additive Manufacturing of an Aircraft Seat

This project explores the redesign of a commercial aircraft seat using AI-assisted generative design and additive manufacturing. The goal was to reduce weight while maintaining strength and passenger safety, ultimately leading to improved fuel efficiency and sustainability in aviation.

Tools used : SolidWorks, ANSYS Workbench, Ultimaker Cura, Autodesk Fusion 360

## Overview

Traditional aircraft seats are often over-designed to ensure safety, leading to unnecessary material usage and increased fuel consumption. This project uses modern engineering tools and generative design techniques to create a structurally sound seat optimized for 3D printing, making it lightweight and manufacturing-efficient.

## Objectives

- Reduce the overall weight of the aircraft seat structure
- Ensure compliance with aviation safety standards
- Optimize the seat design for additive manufacturing (DMLS)
- Minimize material wastage and support sustainable production

## Tools and Software Used

| Tool               | Purpose                                      |
|-------------------|----------------------------------------------|
| SolidWorks        | CAD modeling of the initial seat design      |
| Fusion 360        | Generative design and topology optimization  |
| ANSYS Workbench   | FEA for stress and deformation analysis      |

## Methodology

1. **Initial CAD Modeling**
   - A base seat frame was modeled using SolidWorks, considering ergonomics and typical commercial seat dimensions.

2. **Generative Design (Fusion 360)**
   - Design constraints such as load cases, fixed supports, safety factors, and manufacturing method were set. Fusion 360 generated multiple viable lightweight designs using AI-driven generative design algorithms.

3. **Material Selection**
   - The optimized seat frame was prepared for additive manufacturing using **AlSi10Mg**, an aluminum alloy well-suited for **Direct Metal Laser Sintering (DMLS)**.

4. **FEA Validation**
   - ANSYS Workbench was used to validate the selected design under simulated passenger load (~120 kg). The seat design passed all structural tests with a safety factor of 2 and minimal deformation.

5. **3D Printing Compatibility**
   - The final design was exported for 3D printing, demonstrating suitability for production via DMLS with minimal post-processing.

## Results

- Achieved up to **47% weight reduction** in the seat frame
- All generative designs maintained a **safety factor ≥ 2**
- The final structure met stress and deformation requirements
- Reduced material usage and enabled **eco-conscious manufacturing**

## Key Technical Highlights

- **Multidisciplinary Approach**: Combines mechanical design, finite element analysis, AI-driven generative algorithms, and advanced manufacturing techniques.
- **AI & Generative Design**: AI-assisted Fusion 360 generated multiple design candidates automatically, reducing manual iterations.
- **Sustainability**: Significant reduction in waste and material, contributing to eco-friendly aerospace engineering practices.

# Design Optimization and Additive Manufacturing of an Aircraft Seat

This repository presents a research-backed project focused on the design, optimization, and additive manufacturing of an aircraft seat structure. The goal was to reduce the weight of the component while maintaining structural integrity through generative design and topology optimization.

## Overview

Aircraft seat structures contribute significantly to the overall weight of the cabin interior. Traditional designs are often overengineered due to safety considerations. This project leverages modern engineering tools to reimagine the seat support structure using:

- Topology optimization techniques
- Finite element analysis (FEA)
- Additive manufacturing methods (3D printing)

The process integrates simulation-based load conditions and advanced optimization algorithms to remove unnecessary material and produce a structurally sound, lightweight seat frame.

## Key Figures from the Study

The following figures provide an overview of the optimization pipeline, simulation results, and final manufacturable outcomes. These are drawn from the original publication and provide context for each stage of the workflow.

### Figure 1: Aircraft Seat

This figure shows the Topology Optimization on Fusion 360 . It forms the base model for all optimization and analysis steps.
A mesh with feature size 1 mm was created and loads were applied accordingly, following which the stress distribution was obtained in the simulation shown in the figure. 
<img width="497" height="282" alt="image" src="https://github.com/user-attachments/assets/43173382-7f71-485f-bffb-99b2ecfedcd5" />


### Figure 2:  Post-Processing after topology optimization

This figure illustrates On performing topology optimization in Fusion 360 for the seat leg, the following simulation was set up. This mesh object was further post-processed using the same software through the Promote to Design 
Workspace option.
<img width="374" height="252" alt="image" src="https://github.com/user-attachments/assets/bb995d88-34be-4d30-af00-adb6862fa287" />

---

### Figure 3: Optimized Topology from Generative Design

This figure displays the output of the topology optimization process. It visualizes how material is removed from low-stress areas to reduce weight without compromising safety.
The same is carried out for the cushion and arm rest. 

<img width="635" height="300" alt="image" src="https://github.com/user-attachments/assets/be9cce97-98ee-405f-baa2-57db7d3c8001" />

---
### Figure 4 : Von Mies Stress Distribution
Stress analysis was perfomed in Ansys R19.2 for 5 lattice structures, to idenitify the strongest lattice. 
<img width="1084" height="609" alt="image" src="https://github.com/user-attachments/assets/8530f268-2d52-406c-8931-b0b3ecc87c82" />
Results indicate Honeycomb is the strongest structure.

## Lattice Structure Analysis

The table below summarizes the total deformation results for different lattice structures under a constant compressive load of **1000 N**.  
Lower deformation values indicate stronger and stiffer structures.

| Lattice Structure      | Compressive Load (N) | Total Deformation (mm) |
|------------------------|----------------------|-------------------------|
| Honeycomb              | 1000                 | 0.32016e-5              |
| Octet                  | 1000                 | 3.1092e-5               |
| Body Centered Cube     | 1000                 | 18.825e-5               |
| Face Centered Cube     | 1000                 | 20.256e-5               |
| Diamond                | 1000                 | 26.97e-5                |

### Conclusion
Among the analyzed structures, the **Honeycomb lattice** exhibited the **lowest total deformation (0.32016e-5 mm)** under compression, making it the **strongest and most rigid configuration** for load-bearing applications.

---
### Figure 5: Static Analysis

This figures show the stress distribution across the optimized design under applied loads. It verifies that the structure meets safety and performance thresholds required for aerospace components.

<img width="476" height="262" alt="image" src="https://github.com/user-attachments/assets/1354e8a9-c554-48a7-8a81-db2f781081b6" />
<img width="1132" height="313" alt="image" src="https://github.com/user-attachments/assets/924f0c5f-350c-4d5f-b692-3d8e96cc9a8f" />

---

### Figure 6: Mass vs Minimum Factor of Safety

The scatter plot below illustrates the trade-off between structural safety and mass, highlighting that lightweight designs (~1.5 kg) can achieve high safety margins, making them ideal for aerospace applications.
<img width="588" height="346" alt="image" src="https://github.com/user-attachments/assets/7a7512bf-39d7-41e4-aaed-1161888fc391" />

---

## Methodology Summary

- CAD modeling was done in SolidWorks
- Simulation and optimization were performed using ANSYS Workbench
- Generative design techniques followed topology optimization principles
- Manufacturing feasibility was confirmed via 3D printing of a scaled-down prototype

## Objective

The objective of this project was to **reduce the overall mass of an aircraft seat structure** while maintaining its structural integrity and comfort. This was achieved using **generative design** and **topology optimization** techniques integrated with **additive manufacturing** workflows.

## Mass Reduction Results

The table below summarizes the optimization results for various seat components, showing significant weight reduction across all parts while ensuring mechanical strength and manufacturability.

| Component                      | Method Applied          | Software Used | Initial Mass (kg) | Final Mass (kg) | Reduction in Mass (%) |
|--------------------------------|--------------------------|----------------|------------------:|----------------:|----------------------:|
| Seat leg                       | Generative Design        | Fusion 360     | 25.419           | 1.494           | 94.11                |
| Seat leg                       | Topology Optimization    | Fusion 360     | 25.419           | 10.610          | 58.25                |
| Seat leg                       | Topology Optimization    | nTopology      | 8.742            | 4.510           | 48.41                |
| Arm rest                       | Shell and Lattice infill | nTopology      | 1.207            | 0.632           | 47.58                |
| Seat cushion (Back)            | Shell and Lattice infill | nTopology      | 1.310            | 0.621           | 52.78                |
| Seat cushion (Under Thigh)     | Shell and Lattice infill | nTopology      | 0.405            | 0.267           | 34.10                |

### Conclusion

The optimization methods successfully achieved **up to 94.11% weight reduction** in the seat leg using **Fusion 360’s generative design**, confirming that the project met its objective of developing a **lightweight, structurally efficient, and manufacturable aircraft seat design**.

## Paper Reference

This project is based on the research published in the AIP Conference Proceedings.

**Citation**: [AIP Conference Proceedings – DOI:10.1063/5.0148590](https://doi.org/10.1063/5.0148590)

## License

This repository is shared for educational and non-commercial research use. For reuse or citations, please reference the published paper.

### Reference

This project was published in the AIP Conference Proceedings. You can access the full paper here: [https://doi.org/10.1063/5.0148590](https://doi.org/10.1063/5.0148590)
