# Darcy–Stokes Coupled Solver

## Description
This project implements a solver for the coupled **Darcy–Stokes problem** on a 2D domain.  
The domain is split into two subdomains:
- **Left**: Stokes equations  
- **Right**: Darcy equations  

The coupling is enforced iteratively on the interface using a residual-based fixed-point algorithm.  
The code is written in **C++** with the [deal.II](https://www.dealii.org/) finite element library.

---

## Repository Structure
```
├── src/                # Source code
│   ├── main.cpp        # Entry point
│   ├── Darcy.hpp/.cpp  # Darcy solver
│   ├── Stokes.hpp/.cpp # Stokes solver
|   meshes              # 2 example meshes
├── CMakeLists.txt      # Build configuration
└── README.md           # This file
```

---

## Compilation
Requirements: **CMake** and **deal.II**.
Download the meshes folder from: https://drive.google.com/drive/folders/1b53ZrOJ64bX6KrA3baiffa9-QB8Bxg3C?usp=share_link

```bash
# Clone the repository
git clone https://github.com/FrancescoEgidioFaggion/Faggion_Silvestri_DarcyStokesProblem/tree/main
cd Faggion_Silvestri_DarcyStokesProblem

# Create build directory
mkdir build && cd build

# Run CMake
cmake ..

# Compile
make
```

The executable will be available in:
```
build/coupled_executable
```

---

## Run
Execute the program with:
```bash
./coupled_executable
```

Polynomial degrees and solver settings can be modified in `src/main.cpp`.

---

## Tests
Sample tests are implemented:
 **Manufactured solution with trigonometric functions** 
 **Manufactured solution with polynomial functions**


---

## Authors
Francesco Egidio Faggion 
Silvestri Martina

