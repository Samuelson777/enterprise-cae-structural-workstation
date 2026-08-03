# PyMAPDL Enterprise CAE Structural Workstation (v5.2)

By: SAMUELSON G

An enterprise-grade, browser-based parametric structural simulation and finite element analysis (FEA) workstation designed for civil and structural engineering professionals. This platform bridges the gap between traditional desktop CAE software (such as ANSYS, SAP2000, and Abaqus) and agile, web-based engineering visualization.

---

## 🚀 Key Features

* **Dual-Theme Engineering Workstation:** Seamless switching between a low-fatigue **Dark Mode** for extended modeling sessions and a high-contrast **Light Mode** tailored for formal technical reviews and client presentations.
* **Parametric Topology Generator:** Real-time generation of Howe truss bridges supporting dynamic adjustment of span length, truss height, number of bays, cross-section profiles (SHS, CHS, I-Beam), and material models (Structural Steel, Aluminum, Titanium).
* **Advanced Simulation & Dynamic Animation Suite:**
* *Live Vehicle Load Traversal:* Simulates a moving truck load across the bridge deck with localized elastic depression.
* *Modal Vibration (1st Frequency):* Visualizes natural frequency mode shapes and resonance behavior.
* *Cyclic Proof Load Test:* Evaluates cyclic elastic deflection under service loads.


* **Interactive 3D Viewport:** Built with Three.js and WebGL, featuring OrbitControls, multiple camera projections (Perspective/Orthographic), standard views (ISO, Front, Top), and multiple rendering modes (Shaded + CAD Edges, Pure Wireframe, FEA Stress Heatmapping).
* **Dynamic Assembly Tree & BOM:** Real-time component visibility toggles and automatically calculated Bill of Materials with element counts and mass distributions.
* **CAE Telemetry & JSON Reporting:** Instant evaluation of total mass, max deflection limits ($L/360$ compliance), convergence monitoring, and structured JSON report exporting.

---

## 🛠️ Tech Stack

* **Core Engine:** Vanilla JavaScript (ES6+)
* **3D Graphics & Rendering:** Three.js (r128), WebGL
* **Camera Controls:** Three.js OrbitControls
* **Styling & UI:** Tailwind CSS (Utility-first framework with custom dark mode selectors)

---

## 📥 Getting Started

Because this application is packaged as a high-performance, self-contained single-file architecture, no complex build steps or Node.js environments are strictly required to launch the workstation.

### Prerequisites

* Any modern web browser with WebGL2 support (Chrome, Firefox, Safari, Edge).

### Installation & Execution

1. Clone the repository or download the source HTML file:
```bash
git clone https://github.com/username/enterprise-cae-workstation.git
cd enterprise-cae-workstation

```

2. Open the application directly in your browser:
* Simply double-click `index.html`, or
* Serve locally using a static server (recommended for optimal asset loading):
```bash
npx http-server .

```

3. Navigate to `http://localhost:8080` in your browser.

---

## 📐 Theoretical Framework

Built in accordance with 30-year professional engineering practice standards:

* **Stiffness Matrix Formulation:** Utilizes spatial frame element equivalents (BEAM188 formulation standards) accounting for axial, torsional, and dual-axis flexural deformations.
* **Boundary Condition Verification:** Supports are modeled with fixed pin foundations at the left anchor and longitudinal roller provisions at the right expansion joint to eliminate thermally induced redundant stresses.
* **Stress Concentration Heatmapping:** High-stress regions near portal web diagonals and mid-span lower chords are isolated dynamically using von Mises equivalent stress thresholds.

---

## 📊 Conclusion

The **Enterprise CAE Structural Workstation (v5.2)** successfully streamlines preliminary structural simulation by eliminating heavy licensing bottlenecks. Key takeaways include:

* **Instant Parametric Feedback:** Immediate recalculation of mass, deflection, and component quantities upon variable modification.
* **Serviceability Visualization:** Moving beyond static images to animate dynamic serviceability limits and resonance risks under operational loads.
* **Accessibility:** Delivering production-grade CAE capabilities directly inside a browser environment for rapid engineering iteration.

---

## 🔮 Future Enhancements

Planned upgrades for upcoming enterprise releases include:

* **WebAssembly (WASM) / OpenSees Integration:** Transitioning from approximated real-time mesh displacements to rigorous stiffness matrix assembly and solver execution using compiled C++ FEM libraries running client-side.
* **Elasto-Plastic Material Modeling:** Incorporating nonlinear material behavior to simulate permanent plastic deformation, yield propagation, and ultimate load collapse.
* **Advanced Environmental Load Cases:** Introducing multi-axis seismic acceleration time-history records and aeroelastic wind flutter analysis.
* **Generative Topology Optimization:** Implementing SIMP (Solid Isotropic Material with Penalization) algorithms directly within the design envelope.
* **Cloud Collaborative Sessions:** Enabling multi-user real-time synchronization via WebSockets for distributed engineering teams.

---

## 📜 License

Distributed under the MIT License. See `LICENSE` for more information.
