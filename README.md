# 🧭Random Walk Simulations in 1D, 2D and 3D

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![Jupyter Notebook](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org/)
[![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-green.svg)](https://matplotlib.org/)
[![Plotly](https://img.shields.io/badge/Plotly-Interactive-blueviolet.svg)](https://plotly.com/)

A comprehensive collection of random walk simulations in 1D, 2D, and 3D with interactive visualizations, animations, and statistical analysis.

<table>
  <tr>
    <th>1D Random Walk</th>
    <th>2D Random Walk</th>
    <th>3D Random Walk</th>
  </tr>
  <tr>
    <td><img src="https://github.com/user-attachments/assets/618ce516-88ed-4921-9fa9-f0f14c87475c" width="300"/></td>
    <td><img src="https://github.com/user-attachments/assets/1ed5ccb8-1146-4921-9354-ab104001f386" width="300"/></td>
    <td><img src="https://github.com/user-attachments/assets/eb71af9f-604f-4b25-8e4e-491bd912776b" width="300"/></td>
  </tr>
</table>

## 📚 Table of Contents

- [📘 Introduction](#introduction)
- [✨ Features](#features)
- [📁 Folder Structure](#folder-structure)
- [🛠️ Setup and Installation](#setup-and-installation)
- [🚀 Usage](#usage)
- [⚠️ Important Notes](#important-notes)
- [📓 Notebook Content Overview](#notebook-content-overview)
- [🎞️ Animation & Visual Assets](#animation--visual-assets)
- [📊 Statistics and Analysis](#statistics-and-analysis)
- [🧩 Interactive Features](#interactive-features)
- [🔬 Advanced Analysis](#advanced-analysis)
- [🔗 References](#references)
- [🤝 Contributing](#contributing)
- [📄 License](#license)


## 📘 Introduction

A random walk is a mathematical object, known as a stochastic or random process, that describes a path that consists of a succession of random steps on some mathematical space such as the integers. This notebook provides a hands-on approach to understanding random walks by:

-   Simulating paths in 1D, 2D, and 3D.
-   Analyzing statistical properties like mean displacement and standard deviation.
-   Visualizing trajectories and distributions using `matplotlib` and `plotly`.
-   Creating interactive animations to observe the walk's evolution over time.
-   Exploring the effects of bias on the walker's path.

## ✨ Features

-   **Multi-Dimensional Simulations:** Explore random walks in 1D, 2D, and 3D space.
-   **Statistical Analysis:** Calculate and visualize mean position, standard deviation, and final position distributions over multiple trials.
-   **Biased Walks:** Simulate and analyze random walks where steps in certain directions are more probable.
-   **Interactive Visualizations:** Utilize `plotly` and `ipywidgets` for dynamic plots.
-   **Animations:** Generate `.mp4` or `.gif` animations of random walks using `matplotlib.animation`.
-   **Quadrant Analysis (2D):** Track the walker's time in each quadrant.
-   **Step Size Comparison (2D):** Analyze the effect of different step sizes.
-   **Simultaneous Walks (3D):** Visualize multiple walkers starting from different positions.

## 📁 Folder Structure

```text
.
├── 🎞️ ANIMATION/
│   ├── 🎞️ 1D/         # Animations for 1D walks (.mp4, .gif)
│   ├── 🎞️ 2D/         # Animations for 2D walks (.mp4, .gif)
│   └── 🎞️ 3D/         # Animations for 3D walks (.mp4, .gif)
├── 🖼️ IMAGES/
│   ├── 🖼️ 1D/         # Static plots for 1D walks (.png, .jpg)
│   ├── 🖼️ 2D/         # Static plots for 2D walks (.png, .jpg)
│   └── 🖼️ 3D/         # Static plots for 3D walks (.png, .jpg)
├── 📊 STATISTICS/     # Optional: CSV or other files with statistical results
├── 🧪 random_walk_notebook.ipynb  # The main Jupyter Notebook file
├── 📦 requirements.txt # List of required Python packages
└── 📄 README.md       # This file
```

## 🛠️ Setup and Installation

You can follow these steps to set up your environment and run the notebook.

### ✅ Prerequisites

-   Python 3.7 or higher
-   `pip` (Python package installer)
-   `git` (for cloning the repository)

### 🧬 Cloning the Repository

```bash
git clone <your-repository-url> # Replace <your-repository-url> with the actual URL
cd <repository-directory-name> # Navigate into the cloned directory
```

### 🧰 Setting Up a Virtual Environment (Recommended)

Using a virtual environment prevents dependency conflicts.

1.  **Create a virtual environment** (e.g., named `randomwalk_env`):
    ```bash
    python -m venv randomwalk_env
    ```
2.  **Activate the environment**:
    -   **Windows**:
        ```bash
        randomwalk_env\Scripts\activate
        ```
    -   **Linux/macOS**:
        ```bash
        source randomwalk_env/bin/activate
        ```
3.  **(Optional) Upgrade pip**:
    ```bash
    python -m pip install --upgrade pip
    ```

### 📦 Installing Dependencies

Install all required Python libraries using the `requirements.txt` file:

```bash
pip install -r requirements.txt
```

Alternatively, install them manually:

```bash
pip install numpy scipy scikit-learn matplotlib plotly ipywidgets pandas tqdm ipympl
```
> **Note**: FFmpeg is necessary to save animations in .mp4 format and must be installed manually (see Important Notes below).

## 🚀 Usage

### ▶️ Running the Notebook

1.  Ensure your virtual environment is activated.
2.  Navigate to the repository directory in your terminal.
3.  Launch Jupyter Notebook or JupyterLab:
    ```bash
    jupyter notebook
    # OR
    jupyter lab
    ```
4.  Open the `random_walk_notebook.ipynb` (or your actual notebook file name) in the Jupyter interface.
5.  Run the cells sequentially or explore specific sections.


## ⚠️ Important Notes

This notebook contains interactive visualizations, animations, and data manipulation tools. Follow these instructions to avoid common errors and ensure smooth execution:

- **Animation in Jupyter:**
  - Install the `ipympl` package with:
    ```bash
    pip install ipympl
    ```
  - Use the following magic commands at the top of your notebook:
    ```python
    %matplotlib ipympl  # For displaying animations
    %matplotlib widget  # For interactive widgets
    ```
  - **Tip:** Use only one magic command in a cell depending on your requirements.

- **Saving Animations as .mp4:**
  - **Install FFmpeg:**  
    - **Windows:**
      - Download FFmpeg from [ffmpeg.org](https://ffmpeg.org/download.html).
      - Extract and add the `bin` folder to your system's **PATH**.
    - **macOS/Linux:**
      ```bash
      brew install ffmpeg     # For macOS with Homebrew
      sudo apt install ffmpeg # For Ubuntu/Debian
      ```
    
- **General Tips:**
  - Use `FuncAnimation` from `matplotlib.animation` for creating animations.
  - Utilize `PillowWriter` if you prefer saving animations as `.gif`.
  - Use `tqdm` for progress tracking in loops or simulations.
  - Suppress unnecessary warnings:
    ```python
    import warnings
    warnings.filterwarnings("ignore")
    ```
  - Use Python’s `traceback` module for inline error logging during debugging.

> **Reminder:** Always restart the kernel after switching `%matplotlib` backends or installing new Jupyter-related packages to avoid rendering issues.

## 📓 Notebook Content Overview

The notebook is divided into sections exploring random walks in increasing dimensions:

### 1. One-Dimensional Random Walk

-   **Simulation:** Basic simulation of a single 1D random walk.
  
    <img src="https://github.com/user-attachments/assets/0c14cd17-b715-427e-a320-e031fc0c28b1" width="500"/>
    
-   **Analysis:** Calculating displacement and distance from the origin.
  
    <img src="https://github.com/user-attachments/assets/7c5b3bdf-4373-4422-beb8-7ebde2d88f5e" width="500"/>
    
-   **Multiple Trials:** Running simulations multiple times to observe average behaviour.
  
    <img src="https://github.com/user-attachments/assets/f9338e2d-2478-441a-bf28-cac245ab6b31" width="500"/>
    
-   **Biased Random Walk:** Introducing probabilities for moving left or right.

   | Probability p=0.7 | Probability p=0.3 |
   |--------------------|--------------------|
   | ![1DRandomWalk_trials_p_0.7](https://github.com/user-attachments/assets/d184b08b-ebe8-4a2f-a8f7-d593fc5051c4) | ![1DRandomWalk_trials_p_0.3](https://github.com/user-attachments/assets/6a3c8e79-b851-415f-9b7f-852adccdedf5) |
   
-   **Mean and Standard Deviation Analysis:** Examining how mean position and standard deviation evolve.
  
    <img src="https://github.com/user-attachments/assets/9ca67b0d-445b-4bbe-8e11-c22f28cdb968" width="500"/>

-   **Distribution of Walker's Position:** Visualizing the probability distribution of the walker's position after N steps.
  
    <img src="https://github.com/user-attachments/assets/b1765a36-6666-409d-b003-18a9cec7c085" width="500"/>

-   **Animation:** Animating the 1D random walk.
-   **Animation with Position Distribution:** Animating the walk alongside its evolving position distribution.
  
    https://github.com/user-attachments/assets/16632f80-47e6-4004-bcc5-fdd6bf63c350


### 2. Two-Dimensional Random Walk

-   **Simulation & Plotting:** Simulating and plotting a 2D walk using `matplotlib` and `plotly`.
-   **Contour Plot:** Visualizing the density of visited locations.
-   **Quadrant Analysis:** Tracking the proportion of time spent in each quadrant.
-   **Quadrant Analysis with Animation:** Animating the walk and the evolving quadrant distribution.
-   **Analysis with Contour Plot and Heatmap:** Combined visualization of path and visit frequency.
-   **Distribution of Walker's Position:** Analyzing the 2D distribution of positions over multiple trials.
-   **Distribution of Final Position:** Visualizing where walkers end up after N steps.
-   **Animation:** Basic animation of the 2D random walk path.
-   **Animation with Position Frequency:** Animating the walk alongside a heatmap of visited positions.
-   **Step Size Comparison:** Analyzing walks with different step lengths.
-   **2D Biased Random Walk:** Implementing bias in movement directions (e.g., tendency to move North-East).
-   **Comparison with/without Bias:** Visual comparison of biased vs. unbiased walks.
-   **Biased Walk with Different Probabilities:** Exploring various bias configurations.

### 3. Three-Dimensional Random Walk

-   **Simulation (Single Trial):** Simulating and visualizing a single walk in 3D space using `matplotlib` or `plotly`.
-   **Simulation (Multiple Trials):** Running and analyzing multiple 3D walks.
-   **Multiple Trials with Different Initial Positions:** Simulating walkers starting from various points.
-   **Distribution of Walker's Final Position:** Visualizing the 3D distribution of endpoints.
-   **Simultaneous Random Walk:** Animating multiple walks concurrently.
-   **Biased Random Walk:** Introducing directional bias in 3D steps.
-   **Visualize Biased Walks with IpyWidgets:** Using widgets to explore different bias parameters interactively.
-   **Comparison with/without Bias:** Comparing trajectories of biased and unbiased 3D walks.

## 🎞️ Animation & Visual Assets

Animations and visual outputs are organized into separate directories by dimensionality:

- **ANIMATION/1D/** – Animations for 1D random walk.
- **ANIMATION/2D/** – Animations for 2D random walk.
- **ANIMATION/3D/** – Animations for 3D random walk.
- **IMAGES/1D/**, **IMAGES/2D/**, **IMAGES/3D/** – Supporting images and figures.

Please feel free to add, update, or replace assets as your experiments change.

---

## 📊 Statistics and Analysis

The **STATISTICS** folder is intended for:
- Storing detailed statistical reports and datasets related to random walk experiments.
- Tracking parameters such as mean, variance, skewness, and other performance metrics of the simulations.

This modular organization makes maintaining a historical record of simulation outcomes and analysis easier.

## 🧩 Interactive Features

The notebook includes several interactive components:
- Adjustable parameters for walk length, bias, and step size
- Real-time visualization updates
- Animated simulations with playback controls
- Parameter exploration with ipywidgets
- Statistical analysis with immediate feedback


## 🔬 Advanced Analysis

Statistical investigations included in the notebook:
- Mean square displacement analysis
- First return times
- Probability distributions
- Central limit theorem demonstrations
- Quadrant occupation statistics
- Bias effects on displacement

## 🔗 References
- [Matplotlib Animation Guide](https://matplotlib.org/stable/api/animation_api.html)
- [Plotly Documentation](https://plotly.com/python/)
- [Jupyter ipympl Documentation](https://jupyter-matplotlib.readthedocs.io/en/latest/)
- [FFmpeg Installation](https://ffmpeg.org/download.html)
- [Wikipedia: Random Walk](https://en.wikipedia.org/wiki/Random_walk)
- Lawler, G. F., & Limic, V. (2010). [Random walk: a modern introduction](https://www.cambridge.org/core/books/random-walk/4F74E8A6F7D12BA0A4120EAA269FF301) (Vol. 123). Cambridge University Press.
- Mörters, P., & Peres, Y. (2010). [Brownian motion](https://www.cambridge.org/core/books/brownian-motion/6F65008C62F2BDAC07C8DAA53CB7D6B7) (Vol. 30). Cambridge University Press.
- Spitzer, F. (2013). [Principles of random walk](https://link.springer.com/book/10.1007/978-1-4613-9413-0) (Vol. 34). Springer Science & Business Media.
- Rudnick, J., & Gaspari, G. (2004). [Elements of the random walk](https://www.cambridge.org/core/books/elements-of-the-random-walk/1217EF4C1DD11B790B1B2DA2550AE007): an introduction for advanced students and researchers. Cambridge University Press.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository.
2. Create your feature branch (`git checkout -b amazing-feature`).
3. Commit your changes (`git commit -m 'Add some amazing feature'`).
4. Push to the branch (`git push origin amazing-feature`).
5. Open a Pull Request.


## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.
