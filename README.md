# lubon-visualization
"Interactive 3D visualization of the Lubón particle, linked to the Riemann zeta function zeros."

# 3D Visualization of the Lubón Particle

This repository provides an interactive 3D visualization of the hypothetical **Lubón (Lub)** particle, a scalar boson linked to the non-trivial zeros of the Riemann zeta function \( \zeta(s) \). The visualization is implemented in a Jupyter Notebook, optimized for [Binder](https://mybinder.org/), and features animations, sliders, and detailed annotations.

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/your-username/lubon-visualization/main)

## Overview

The Lubón particle is a theoretical construct with the following properties:
- **Type**: Scalar boson (spin-0)
- **Mass**: ~10⁻³ eV/c² (lighter than neutrinos)
- **Energy**: \( E_n = \hbar \omega \gamma_n \), where \( \gamma_n \) are the imaginary parts of the zeta function's non-trivial zeros
- **Nature**: Resonance in a quantum system with chaotic dynamics (GUE statistics)
- **Connection**: Defined by the Riemann zeta function \( \zeta(s) \)
- **Potential Detection**: Quantum dots, photonic crystals, or cosmological observations
- **Dark Matter**: Possible candidate
- **Significance**: A bridge between mathematics and physics

The visualization plots the probability density \( |\text{lub}_n(t)|^2 \) and the effective potential \( V_{\text{eff}}(t) = -k |\zeta(1/2 + it)|^2 \) in 3D space, corresponding to the first three zeros (\( \gamma_1 = 14.1347 \), \( \gamma_2 = 21.0220 \), \( \gamma_3 = 25.0108 \)).

## Features
- **Exact Eigenfunctions**: Computes \( \text{lub}_n(t) \) as eigenfunctions of the operator \( \hat{H} \) with kernel \( K_{\text{sym}}(t, t') \).
- **Animation**: Visualizes the phase evolution \( e^{-i \omega \gamma_n t} \) with "Play"/"Pause" buttons.
- **Sliders**: Allows switching between \( \gamma_n \) for different \( |\text{lub}_n(t)|^2 \).
- **Annotations**: Marks \( \gamma_n \) positions on the graph.
- **Surface Plot**: Displays a semi-transparent surface for \( V_{\text{eff}}(t) \).
- **Centered Visualization**: Graph is centered with optimized camera angles.
- **Export**: Saves the plot as `lubon_visualization.html` for offline viewing.
- **Colors**:
  - Blue: \( |\text{lub}_1(t)|^2 \) (\( \gamma_1 = 14.1347 \))
  - Green: \( |\text{lub}_2(t)|^2 \) (\( \gamma_2 = 21.0220 \))
  - Purple: \( |\text{lub}_3(t)|^2 \) (\( \gamma_3 = 25.0108 \))
  - Red (dashed): \( V_{\text{eff}}(t) \)
  - Red (semi-transparent): Surface of \( V_{\text{eff}}(t) \)

## How to Use
1. **Launch in Binder**:
   - Click the Binder badge above or visit [mybinder.org](https://mybinder.org/) and enter the repository URL (`https://github.com/YYurq/lubon-visualization`).
   - Wait for the environment to load.
2. **Run the Notebook**:
   - Open `binder-lubon.ipynb`.
   - Execute the first cell to install dependencies.
   - Execute the second cell to generate the visualization.
3. **Interact**:
   - Use sliders to switch between \( \gamma_n \).
   - Click "Play"/"Pause" for animation.
   - Rotate and zoom the 3D plot.
   - Download `lubon_visualization.html` for offline use.
4. **Local Setup** (optional):
   - Clone the repository:
     ```bash
     git clone https://github.com/YYurq/lubon-visualization.git
     cd lubon-visualization
     ```
   - Create a virtual environment and install dependencies:
     ```bash
     python -m venv env
     source env/bin/activate  # On Windows: env\Scripts\activate
     pip install -r requirements.txt
     ```
   - Run the notebook:
     ```bash
     jupyter notebook binder-lubon.ipynb
     ```

## Repository Structure
- `binder-lubon.ipynb`: Jupyter Notebook with the visualization code.
- `requirements.txt`: Python dependencies.
- `environment.yml`: Binder environment configuration.
- `.github/workflows/binder.yml`: GitHub Actions for Binder automation.
- `README.md`: This file.

## Dependencies
- Python 3.11
- numpy==1.26.4
- matplotlib==3.9.2
- mpmath==1.3.0
- scipy==1.14.1
- plotly==5.24.1
- sympy==1.13.3

## Results
The notebook generates an interactive 3D plot with:
- Animated probability densities \( |\text{lub}_n(t)|^2 \) for three zeta zeros.
- Effective potential \( V_{\text{eff}}(t) \) as a dashed line and semi-transparent surface.
- Annotations marking \( \gamma_n \).
- Sliders for selecting different \( \gamma_n \).
- Centered visualization with export to HTML.
- Console output describing the Lubón particle and color legend.

## Notes
- The eigenfunctions \( \text{lub}_n(t) \) are computed numerically, which may take a few seconds in Binder.
- For faster performance, reduce the number of points (e.g., change `t = np.linspace(-T, T, 300)` to `200`).
- The animation uses a short time interval (\( 10^{-12} \, \text{s} \)) for clarity; adjust `time` in `np.linspace` for longer animations.

## Contributing
Contributions are welcome! Please open an issue or submit a pull request for improvements, such as:
- Enhanced visualizations (e.g., additional animations).
- Optimization of eigenfunction calculations.
- Support for more zeta zeros.

## License
MIT License. See [LICENSE](LICENSE) for details.

## Contact
For questions, contact [y.yurqa@gmail.com](mailto:your-email@example.com).
