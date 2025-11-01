
# CUDA Parallel Reduction and Scan

This project implements **Parallel Reduction (Sum of Array)** and **Prefix Scan (Prefix Sum)** algorithms using **NVIDIA CUDA**.  
It demonstrates how GPU acceleration can significantly improve performance over sequential CPU computation for large datasets.

---

## 🚀 Project Overview

### 🔹 Parallel Reduction
Parallel reduction computes the sum of all elements in an array by dividing the data among multiple CUDA threads and performing a tree-based reduction in shared memory.

### 🔹 Parallel Prefix Scan
Prefix Scan (also known as cumulative sum) computes partial sums of an array using two classic parallel algorithms:
- **Blelloch Scan** (up-sweep and down-sweep phases)
- **Hillis–Steele Scan**

Both demonstrate synchronization, shared memory use, and efficient parallel computation.

---

## 🧠 Learning Objectives
- Understand CUDA thread hierarchy (blocks, threads, grids)
- Implement parallel algorithms using shared and global memory
- Compare CPU and GPU execution performance
- Analyze efficiency and speed-up gained via GPU computation

---

## ⚙️ Requirements
- NVIDIA GPU with CUDA support  
- CUDA Toolkit (v10.0 or later)  
- GCC / G++ compiler  

---

## 🧩 Compilation and Execution

### 1. Clone the repository
```bash
git clone https://github.com/<your-username>/cuda-parallel-reduction-scan.git
cd cuda-parallel-reduction-scan
````

### 2. Compile and Run

#### For Reduction:

```bash
nvcc reduction.cu -o reduction
./reduction
```

#### For Scan:

```bash
nvcc scan.cu -o scan
./scan
```

---

## 📊 Example Output

**Sample Output (for Reduction):**

```
CPU Sum:  500000000
GPU Sum:  500000000
Speed-up: 15.2x
```

**Sample Output (for Scan):**

```
Input Array:  [1, 2, 3, 4, 5]
Prefix Sum:   [1, 3, 6, 10, 15]
Execution Time (GPU): 0.05 ms
```

---

## 📈 Results and Discussion

| Array Size | CPU Time (ms) | GPU Time (ms) | Speed-up |
| ---------- | ------------- | ------------- | -------- |
| 1,000,000  | 45.2          | 3.1           | 14.6x    |
| 10,000,000 | 461.7         | 25.4          | 18.2x    |

GPU acceleration provides clear performance benefits for large-scale data processing tasks due to massive thread-level parallelism.

---

## 🧾 References

* NVIDIA CUDA Programming Guide
* Mark Harris, “Optimizing Parallel Reduction in CUDA”
* GitHub Repository: [huschen/cuda_programming](https://github.com/huschen/cuda_programming)

---

## 👨‍💻 Author

**Manthan S**
Bachelor of Engineering in Computer Science
The Oxford College of Engineering (VTU)
Subject: *Parallel Computing*

```

