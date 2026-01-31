<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white" />
  <img src="https://img.shields.io/badge/Matplotlib-ffffff?style=for-the-badge&logo=matplotlib&logoColor=black" />
  <img src="https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge" />
</p>

<h1 align="center">Gradient Descent: Optimizing Theta Values</h1>

<p align="center">
  A robust implementation of <b>Logistic Regression</b> using <b>Gradient Descent</b> to find optimal θ (theta) values. This project demonstrates the mathematical foundations of machine learning, featuring L2 regularization, convergence monitoring, and decision boundary visualization.
</p>

<p align="center">
  <a href="#technical-architecture">
    <img src="https://img.shields.io/badge/Architecture-222222?style=flat" />
  </a>
  <span> ° </span>
  <a href="#project-structure">
    <img src="https://img.shields.io/badge/Structure-222222?style=flat" />
  </a>
  <span> ° </span>
  <a href="#mathematical-foundations">
    <img src="https://img.shields.io/badge/Math-222222?style=flat" />
  </a>
  <span> ° </span>
  <a href="#technical-specifications">
    <img src="https://img.shields.io/badge/Specs-222222?style=flat" />
  </a>
  <span> ° </span>
  <a href="#deployment--installation">
    <img src="https://img.shields.io/badge/Deploy-222222?style=flat" />
  </a>
</p>

---
<br>

<h2 align="center">Technical Architecture</h2>

The core of this project is a custom-built `LogisticRegression` class that implements the optimization loop from scratch. Unlike standard library implementations, this codebase provides deep visibility into the convergence process:

1.  **Iterative Optimization:** Uses Gradient Descent to update theta values until the Euclidean distance between successive iterations falls below a predefined epsilon.
2.  **Regularization (L2):** Incorporates a regularization lambda to prevent overfitting by penalizing large theta coefficients.
3.  **Standardization:** Features a preprocessing pipeline that scales input data (Z-score normalization) to ensure stable gradient steps.
4.  **Convergence Monitoring:** Real-time tracking of the cost function values for debugging and performance verification.

---
<br>

<h2 align="center">Project Structure</h2>

```
ML_GradientDescent-.-FindThetaValues/
├── LICENSE                                   # MIT License
├── README.md                                 # Project documentation
├── .gitattributes                            # Git configuration
├── Project Report.pdf                        # IEEE-style technical report
│
└── Code/                                     # Core Implementation
    ├── logreg.py                             # Reusable Logistic Regression class
    ├── test_logreg1.py                       # Main execution and plotting script
    └── data1.dat                             # Sample dataset (features + labels)
```

---
<br>

<h2 align="center">Mathematical Foundations</h2>

### 1. The Sigmoid Function
Maps any real-valued number into a value between 0 and 1, facilitating probabilistic classification.
```text
hθ(x) = 1 / (1 + e^(-θᵀx))
```

### 2. Regularized Cost Function
The objective function minimized via gradient descent, including the L2 penalty term.
```text
J(θ) = -1/n * Σ [y(i)log(hθ(x(i))) + (1-y(i))log(1-hθ(x(i)))] + λ/2n * Σ θⱼ²
```

### 3. Gradient Update
The parameter update rule applied at each iteration to converge towards the global minimum.
```text
θⱼ := θⱼ - α * [1/n * Σ (hθ(x(i)) - y(i))xⱼ(i) + λ/n * θⱼ]
```

---
<br>

<h2 align="center">Technical Specifications</h2>

<table align="center">
  <tr>
    <th align="center">Parameter</th>
    <th align="center">Description</th>
  </tr>
  <tr>
    <td align="center"><b>Algorithm</b></td>
    <td align="center">Logistic Regression (Regularized)</td>
  </tr>
  <tr>
    <td align="center"><b>Optimization</b></td>
    <td align="center">Vanishing Gradient Descent</td>
  </tr>
  <tr>
    <td align="center"><b>Learning Rate (α)</b></td>
    <td align="center">Configurable (Default: 0.01)</td>
  </tr>
  <tr>
    <td align="center"><b>Regularization (λ)</b></td>
    <td align="center">Configurable (Default: 0.01)</td>
  </tr>
  <tr>
    <td align="center"><b>Convergence (ε)</b></td>
    <td align="center">Distance threshold (Default: 0.0001)</td>
  </tr>
</table>

---
<br>

<h2 align="center">Deployment & Installation</h2>

### Repository Acquisition
Clone the repository and navigate to the project directory:

```bash
git clone https://github.com/Zer0-Bug/ML_GradientDescent-.-FindThetaValues.git
cd ML_GradientDescent-.-FindThetaValues
```

### Setup & Dependencies
It is recommended to use a virtual environment:

```bash
# Create and activate environment
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate

# Install requirements
pip install numpy matplotlib
```

### Execution
Run the test script to execute the training process and visualize the decision boundary:

```bash
python Code/test_logreg1.py
```

---
<br>

<h2 align="center">Contribution</h2>

Contributions are always appreciated. Open-source projects grow through collaboration, and any improvement—whether a bug fix, new feature, documentation update, or suggestion—is valuable.

To contribute, please follow the steps below:

1. Fork the repository.
2. Create a new branch for your change:  
   `git checkout -b feature/your-feature-name`
3. Commit your changes with a clear and descriptive message:  
   `git commit -m "Add: brief description of the change"`
4. Push your branch to your fork:  
   `git push origin feature/your-feature-name`
5. Open a Pull Request describing the changes made.
<br>
All contributions are reviewed before being merged. Please ensure that your changes follow the existing code style and include relevant documentation or tests where applicable.

---
<br>
<h2 align="center">References</h2>

1. **Ng, A.** - [CS229 Lecture Notes: Logistic Regression](https://see.stanford.edu/materials/aimlcs229/cs229-notes1.pdf). *Stanford University*.

---
<br>
<p align="center">
  <a href="mailto:777eerol.exe@gmail.com">
    <img src="https://cdn.simpleicons.org/gmail/D14836" width="40" alt="Email">
  </a>
  <span> × </span>
  <a href="https://www.linkedin.com/in/eerolexe/">
    <img src="https://upload.wikimedia.org/wikipedia/commons/c/ca/LinkedIn_logo_initials.png"
         width="40"
         alt="LinkedIn">
  </a>
</p>

---

<p align="center" style="margin-top:10px; letter-spacing:4px;">
  ∞
</p>
