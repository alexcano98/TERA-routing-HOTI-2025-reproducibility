# TERA: Deadlock-free routing for Full-mesh networks without using Virtual Channels

TERA (Topology-Embedded Routing Algorithm) is a novel deadlock-free routing algorithm for Full-mesh networks. It avoids the need for Virtual Channels (VCs) and achieves higher performance under adversarial and real-application traffic scenarios than other routing alternatives with the same resources.

This repository contains all code, configuration files, and documentation needed to **reproduce the results** in our paper:

> **"Deadlock-free routing for Full-mesh networks without using Virtual Channels"**
> Accepted at **HOT Interconnects (HOTI), 2025**

📄 [📥 PDF (link)](TODO: add link)
📚 Citation: See below

---
## 🚀 Key Features of TERA routing algorithm

* Deadlock-free adaptive routing without Virtual Channels
* Up to 100% speedup against other link-ordering routing algorithms in Full-Mesh.
* Up to 32% speedup against other routing algorithms in a 2D-HyperX network with the same resources.
---

## 📁 Repository Structure

* `caminos/` — Small application which implements the caminos-lib library to run simulations.
* `caminos-lib/` — Library to simulate interconnection networks: [CAMINOS simulator](https://github.com/caminos-simulator/caminos) (commit `abc1234`)
* `simulation_files/` — Config files for reproducing our experiments. Each directory corresponds to a different experiment in the paper. Each directory contains several simulations.
* `USAGE.md` — Full usage & configuration documentation
* `README.md` — Project overview (this file)

---

## ⚙️ Prerequisites

Make sure the [Rust toolchain](https://www.rust-lang.org/tools/install) is installed.

---

## 🧪 Quick Start

This repository includes `caminos` and `caminos-lib` as Git submodules.
To properly clone the repository along with its submodules, use one of the following methods:

```bash
git clone --recurse-submodules https://github.com/alexcano98/TERA-routing-HOTI-2025-reproducibility.git
````
or, if you've already cloned the repository:

```bash
git clone https://github.com/alexcano98/TERA-routing-HOTI-2025-reproducibility.git
cd TERA-routing-HOTI-2025-reproducibility
git submodule update --init --recursive
````

🛠️ To follow the steps below, make sure the [Rust toolchain](https://www.rust-lang.org/tools/install) is installed.

Enter the `caminos` directory and compile the project:
````bash
cd caminos
cargo build --release
````
Now you can run any experiment from the paper! Example:
````bash
cd simulation_files/Figure-5-link-ordering-comparison
../../caminos/target/release . -a local #Runs all the experiments from the directory locally.
````

---

## 📘 Reproducing the Results

See [`USAGE.md`](./USAGE.md) for full instructions on:

* Setting up CAMINOS
* Modifying simulation parameters
* Reproducing specific experiments from the paper

---

## ✉️ Authors & Contact

* Alejandro Cano – Universidad de Cantabria – [alejandro.cano@unican.es](mailto:alejandro.cano@unican.es)
* Cristóbal Camarero – Universidad de Cantabria –[cristobal.camarero@unican.es](mailto:cristobal.camarero@unican.es)
* Carmen Martínez – Universidad de Cantabria –[carmen.martinez@unican.es](mailto:cristobal.camarero@unican.es)
* Ramón Beivide – Universidad de Cantabria and Barcelona Supercomputing Center–[ramon.beivide@unican.es](mailto:ramon.beivide@unican.es)

---

## 📄 Citation

If you use TERA in your work, please cite:

```bibtex
@inproceedings{

}
```

---

## 📜 License

This project is licensed under the MIT License. See [LICENSE](./LICENSE) for details.
