# USAGE.md

## 🛠️ Installation & Setup

This guide will help you set up the environment and run the TERA simulations using the CAMINOS simulator.

---

### 1. Clone the Repository with Submodules

```bash
git clone --recurse-submodules https://github.com/your-username/tera-routing-sim.git
```

If you already cloned the repository without submodules, run:

```bash
git submodule update --init --recursive
```

---

### 2. Compile CAMINOS

Enter the `caminos` directory and build the simulator using Cargo (requires [Rust](https://www.rust-lang.org/tools/install)):

```bash
cd caminos
cargo build --release
```

The CAMINOS binary will be located at:

```bash
target/release/caminos
```

You can symlink or add it to your PATH for convenience.

---

## 🚀 Running Simulations

All simulations used in the paper are organized under the `simulation_files/` directory.
Each directory contains all the simulations corresponding to one Figure of the paper.
The files contained in each directory are:

- `main.cfg`: file which define the parameters for the simulations to run in that directory.
- `main.od`: file which define the parameters to extract plots from the simulations results.
- `outputs/`: directory that stores the plots defined in the main.od
- `runs/`: directory that save the results of all the simulations in the directory. Each simulation result is saved with its configuration file.
- `journal`: file that logs the actions performed in a simulation directory.
- *(Optional)* `remote`: file that stores the credentials of a remote machine to run simulations there.

---

### 1. Run Simulations

Navigate into any simulation directory and run:

```bash
/path/to/caminos . -a local
```

This executes all the configurations defined in `main.cfg`. Simulation results are saved in the `runs/` directory.

---

### 2. Generate Plots

Once simulations are completed, generate output charts using:

```bash
/path/to/caminos . -a output
```

This uses `main.od` to plot performance metrics. Output files will be saved in the `outputs/` directory.

---

### 3. Simulation Parameters

For more information about the simulator run under the `caminos-lib/` directory:
```bash
cargo doc
```

And documentation will be generated at `target/doc/caminos_lib/index.html`.

---



## 📬 Questions or Contributions

Feel free to contact the authors (see `README.md`) or reach out to:

📧 [alejandro.cano@unican.es](mailto\:alejandro.cano@unican.es)

---

Happy simulating! ✨
