# Biomechanical Analysis and FEM Simulation of Circular Seating Systems
Research scholarship | Design and Validation | Politecnico di Milano Academic Year: 2024-2025  

## 📌 Project Overview
This project is part of the Circular Sofa Platform, developed within the MICS (Made in Italy Circolare e Sostenibile) program. The research focuses on replacing traditional polyurethane (PU) foam with sustainable, modular, and fully recyclable seating solutions.

The core of the project is a modular system of thermoplastic elastomer (TPU) cells, designed for easy assembly, disassembly, and circular material management.

## 🛠 My Role: FEM Analyst & Biomechanical Researcher
I managed the end-to-end simulation workflow to validate the digital twins of the circular padding prototypes against experimental data.

### 1. Finite Element Analysis (FEA) & Validation
I performed structural simulations using Abaqus CAE 2022 to replicate physical compression tests and validate the mechanical response of the modular cells.
* Material Characterization: Defined TPU (Shore 90A/D41) properties as a linear elastic material ($E = 90$ MPa, $\nu = 0.48$).
* Numerical Setup: Implemented Explicit Dynamic solvers to effectively manage large deformations and buckling phenomena occurring in the thin-walled cellular structures.
* Assembly Modeling: Analyzed different interaction strategies, utilizing General Contact with a friction coefficient of 0.5 to simulate real-world modular assembly.
* Accuracy: Achieved a high correlation between digital and physical tests, with vertical displacement results showing a consistent <10% error margin compared to experimental benchmarks.

### 2. Human-Product Interaction & Anatomical Modeling
To predict user comfort and pressure distribution, advanced human body models were integrated into the simulation environment. Due to the research's time constraints, the study focused on the initial phase of this integration, which involved defining and isolating the anatomical regions of interest. As a preliminary validation step, a rigid support was utilized instead of the cellular padding to establish a baseline for the human body's mechanical interaction and weight distribution.

* Virtual Anatomy: Utilized the THUMS (Total Human Model for Safety) AM50 model (50th percentile male) and S (Sitting) configurations.

* Model Optimization: Simplified the 2.1-million-element model by isolating the gluteal region. This reduced computational costs while maintaining anatomical accuracy at the contact interface.
    <div align="center">
             <img src="./Images/Set_up.png" align="central" width="800" alt="Stress distribution">
  <p align="center">
    <em><strong>Figure 1:</strong> Final model used for the FEM simulation.</em>
  </p>
* Biomechanical Mapping: Assigned specific material properties to human tissues (Bone: 17.3 GPa; Flesh/Soft Tissue: 1 GPa) and implemented body-weight distribution based on clinical literature. To ensure realistic simulation, loads were    applied to key anatomical landmarks proportional to Body Weight (BW):
                             
  * **Ischial Tuberosities:** 18% BW
  * **Thighs:** 21% BW
  * **Sacrum:** 5% BW
    
<div align="center">
  <img src="./Images/punti_applicazione.jpg" width="300" alt="Pressure Zones Mapping">
  <br>
  <em><strong>Figure 2:</strong> Anatomical Load Distribution Mapping</em>
</div> 

## 📊 Key Findings
* Pressure Mapping: Identified peak stress zones at the ischial tuberosities (approx. 5 kPa), aligning with ergonomic comfort standards.
  <div align="center">
             <img src="./Images/VonMises_pressure.jpg" align="central" width="800" alt="Stress distribution">
  <p align="center">
    <em><strong>Figure 3:</strong> On the left the Von Mises distribution on the skin. On the right Pressure distribution on the muscles.</em>
  </p>


* Validation: Successfully established a methodology to extend physical user testing into a predictive virtual environment, allowing for the analysis of non-measurable parameters like internal stress distribution and heat transfer.

## 💻Software
* **Abaqus**
* **Ansa** 
