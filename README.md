# Matboard Bridge Structural Simulation

This project simulates a **matboard bridge** under a **moving train load** using MATLAB. It computes the **shear force** and **bending moment** distributions across the bridge and evaluates the **failure modes** based on material and geometric properties. The program determines the **factors of safety (FOS)** for various failure types and visualizes how internal forces evolve as the train crosses the bridge.

---

## 🔧 Features

- Simulates a **six-axle train** traversing a 1200 mm simply supported bridge  
- Generates **Shear Force Diagrams (SFD)** and **Bending Moment Diagrams (BMD)** for each train position  
- Calculates:
  - Reaction forces at supports  
  - Flexural, shear, and glue stresses  
  - Local and global buckling stresses  
- Determines **factors of safety** for:
  - Tension and compression  
  - Shear (material and glue)  
  - Buckling (top flange, sides, and webs)  
- Produces plots showing critical failure thresholds alongside actual SFD/BMD envelopes  

---

## 🧮 Engineering Methods

The analysis combines **classical beam theory** with **failure mechanics**:

1. **Static Equilibrium:**  
   Calculates support reactions (`Ay`, `By`) for each train position.

2. **Internal Force Distribution:**  
   Integrates applied loads to produce SFD and BMD envelopes.

3. **Cross-Section Analysis:**  
   Computes the centroid and moment of inertia using the **parallel axis theorem**.

4. **Stress Evaluation:**  
   - Flexural stress:  
     \[
     \sigma = \frac{M y}{I}
     \]
   - Shear stress:  
     \[
     \tau = \frac{VQ}{I b}
     \]

5. **Buckling Analysis:**  
   Applies plate buckling formulas to estimate local instability limits.

6. **Failure Assessment:**  
   Calculates factors of safety for each mode and identifies the governing failure condition.

---

## 📊 Output

The program outputs:

- **SFD and BMD envelopes** for the entire bridge span  
- **Failure threshold lines** for each mode  
- **Minimum factor of safety** and **dominant failure type**  
- Visual plots comparing failure limits with actual forces

Example plots:
- Shear failure (matboard, glue, and buckling)
- Flexural failure (tension, compression, and buckling)
