# Understanding the Google PageRank Algorithm  

---

## Authors
**Madeline Renee Boss**  
**Samhitha Devi Kunadharaju**  
*University of Texas at Austin*  
Course: *CS 323E – Elements of Scientific Computing*

---

## Overview
This project implements and analyzes the **Google PageRank algorithm** using both the iterative update  
`x_{k+1} = Hx_k` and the dominant eigenvector of the hyperlink matrix `H`.  
Two example web networks are evaluated, and both methods converge to the same steady-state PageRank vector.

---

## Included Files

| File | Description |
|------|--------------|
| **`pagerank_analysis.ipynb`** | Jupyter/Colab notebook with hyperlink matrix construction, iterative computation, eigenvector solution, and plots |
| **`PageRank_Paper.pdf`** | Full paper explaning PageRank, linear algebra background, and results |
| **`convergence-6.png`** | PageRank Convergence Behavior for Six-Page Web Network |
| **`convergence-8.png`** | PageRank Convergence Behavior for Eight-Page Web Network |
| **`requirements.txt`** | List of dependencies (NumPy, Matplotlib, SciPy) |


---
## Key Ideas
- The web is modeled as a **directed graph**, producing a **column-stochastic matrix**.  
- PageRank is the **eigenvector of `H` with eigenvalue 1**.  
- Iterative updates and eigenvector computation give the same result (Theorem 4.9).  
- A page is important when **important pages link to it**, not simply by having many links.

---
## Results (Summary)
- **6-page network:** Pages 4, 6, and 5 retain all rank; pages 1–3 converge to zero.  
- **8-page network:** All pages have nonzero rank; Page 4 is the most influential.

## How to Run
```bash
pip install -r requirements.txt
