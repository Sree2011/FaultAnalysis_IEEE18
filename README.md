# IEEE 18 bus system Fault Analysis 🔌⚡

Tools used:\
[`Octave`](https://www.gnu.org/software/octave/)  
[`Visual Studio Code`](https://code.visualstudio.com/)  
[`MATLAB`](https://www.mathworks.com/products/matlab.html) (for compatibility)

This project implements **load flow analysis, symmetrical components, and fault current calculations** for the IEEE 18‑bus test system using GNU Octave/Matlab. It is designed to be modular, reproducible, and recruiter‑ready, with clear outputs and organized results.

---

## 📂 Project Structure

```
IEEE18_FaultAnalysis/
├── data/          # Input data (busdata.m, linedata.m, gendata.m)
├── core/          # Core functions for load flow and    fault analysis(fault_current_3ph.m, fault_current_slg.m, etc.)
├── results/       # Auto-saved plots and outputs
├── scripts/
    ├── run_fault.m # Fault analysis driver script
    ├── main.m  # Main driver script
    ├── run_loadflow.m # Load flow analysis
    ├── visualize.m # Plotting functions
└── README.md      # Documentation
```

---

## 🚀 Features

- **Newton–Raphson Load Flow**
  - Computes bus voltages (magnitude & angle).
  - Calculates active/reactive power injections.
  - Saves recruiter‑ready plots into `results/`.

- **Symmetrical Components**
  - Forward transform: $V_a, V_b, V_c \rightarrow V_0, V_1, V_2$.
  - Inverse transform: $V_0, V_1, V_2 \rightarrow V_a, V_b, V_c$.
  - Phasor diagrams with distinct colors for clarity.

- **Fault Analysis**
  - Single Line‑to‑Ground (SLG).
  - Line‑to‑Line (LL).
  - Double Line‑to‑Ground (DLG).
  - Three‑Phase (balanced).
  - Outputs both magnitude and angle of fault currents.

- **Automation**
  - All plots saved automatically into `results/`.
  - Tabular printouts for bus results and fault currents.
  - Modular design for easy extension.

---

## 🖥️ Usage

1. Clone the repository:
   ```bash
   git clone https://github.com/Sree2011/IEEE18_FaultAnalysis.git
   cd IEEE18_FaultAnalysis
   ```

2. Open GNU Octave or Matlab.

3. Run the main script:
   ```octave
   octave main.m(if using command line)
   ```

4. Check the `results/` folder for plots and outputs.

---

## Documentation
- Documentation is published in HTML format using Texinfo, generated from '.texinfo' files.
- [Fault current functions](docs/texinfo/fault_current.html/index.html)
- [Symmetrical components functions](docs/texinfo/symmetrical_components.html/index.html)
- [Load flow functions](docs/texinfo/load_flow.html/index.html)


## 📊 Example Outputs

- **Bus Voltages**: Magnitude and angle at each bus.
- **Power Injections**: Active (P) and reactive (Q).
- **Symmetrical Components**: $V_0, V_1, V_2$ at selected bus.
- **Fault Currents**: Side‑by‑side comparison of SLG, LL, DLG, and 3‑phase faults.

---

## 🛠️ Requirements

- GNU Octave (recommended) or Matlab.
- VS Code with Octave extension (optional, for syntax highlighting).
- `vscode-icons` theme for Octave icon support.

---

## 📌 Next Steps

- Add transient stability analysis.
- Export consolidated reports (PDF/CSV).
- Extend to larger IEEE test systems.

---

## ✨ Motivation

Although documentation wasn’t strictly necessary, it was created to highlight the **clarity, automation, and recruiter‑ready presentation** of this workflow. This project reflects an iterative approach: modular scripts, organized outputs, and polished visuals.

---
## 📝 Note on GNU Octave vs Matlab

- This project was developed entirely in **GNU Octave** because I do not have a subscription for Matlab.  
- Octave is a free, open-source alternative that supports most Matlab syntax, so all `.m` files in this repository are **Matlab-compatible**.  

- Functions and scripts follow Matlab conventions (`.m` files).  
- Docstrings are written in **Texinfo format**, which Octave uses for help and documentation.  
- Documentation can be generated using **pkg-octave-doc** (Octave’s equivalent of Javadoc).
- Matlab users can still run these files directly, though some plotting or package calls may differ slightly.
---

## References
1. IEEE 18-bus system data: [Github Repo](https://github.com/MilosFTN/Models-of-the-IEEE-18--and-33-bus-test-systems)

2. Load flow analysis and symmetrical components: [Power System Analysis by Hadi Saadat](https://www.amazon.com/Power-System-Analysis-Hadi-Saadat/dp/0073380169)

<script type="text/javascript" async
  src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js">
</script>