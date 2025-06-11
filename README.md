# PSO_CUDA_Project

A parallel implementation of the Particle Swarm Optimization (PSO) algorithm using **CUDA C** and **Python**, inspired by **SPSO2011** and tested on benchmark functions like **Sphere** and **Schaffer F7**.

---

##  Project Structure

PSO_CUDA_Project/
│
├── src/                               # All source code (modularized)
│   ├── PSO_Sequential.py              # CPU version of PSO (SPSO2011)
│   ├── PSO_Parallel.cu                # GPU version with CUDA kernel (1 run)
│   ├── PSO_Parallel_MultiBlock.cu     # GPU with multiblock (51 runs)
│   ├── PSO_Parallel_Shared.cu         # Shared memory optimized version
│   ├── limits.cu                      # Floating-point GPU tests
│   ├── shared_memory_test.cu         # Shared memory test utility
│   └── utils.py                       # Common Python helpers: obj fn, init, plot
│
├── notebooks/                         # Google Colab notebooks
│   └── main.ipynb                     # Central controller notebook (runs all)
│
├── dataset/                           # Input/output datasets
│   ├── input.txt                      # (optional input)
│   └── output_results.csv             # Final results from CPU/GPU
│
├── results/                           # All PSO outputs for comparison
│   ├── cpu_logs.txt
│   ├── gpu_logs.txt
│   └── summary.csv
│
├── img/                               # Visuals and plots
│   ├── pso_convergence_cpu.png
│   ├── pso_convergence_gpu.png
│   └── topology_art.png
│
├── README.md                          # Project overview and run guide
├── requirements.txt                   # Python library list (for Colab)



---

## How to Run (on Google Colab)

1. **Mount Google Drive** in Colab:
```python
from google.colab import drive
drive.mount('/content/drive')


cd /content/drive/MyDrive/PSO_CUDA_Project/notebooks/
