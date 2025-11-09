# Parametric Curve Assignment

## Objective
Estimate the unknown variables θ, M, and X in the given parametric curve equations so that the predicted curve fits the dataset accurately.

---

## Final Optimized Parameters
- θ (degrees): 28.1209  
- M: 0.0214  
- X: 54.9011  

---

## Final Equation (LaTeX Format)
\left(t*(cos(28.1209)-e^(0.0214*|t|)*sin(0.3t)sin(28.1209))+54.9011, 42+t*sin(28.1209)+e^(0.0214*|t|)*sin(0.3t)cos(28.1209)\right)

---

## Methodology
1. Loaded the dataset `xy_data.csv` which contains the (x, y) points for 6 < t < 60.
2. Defined the given parametric curve equations:
   - x(t) = (t·cos(θ) - e^(M|t|)·sin(0.3t)·sin(θ)) + X  
   - y(t) = (42 + t·sin(θ) + e^(M|t|)·sin(0.3t)·cos(θ))
3. Generated t values linearly spaced between 6 and 60.
4. Defined an objective function that minimizes the L1 distance between predicted and actual (x, y) coordinates.
5. Used SciPy’s L-BFGS-B optimizer to find θ, M, and X within their allowed ranges:
   - 0° < θ < 50°  
   - -0.05 < M < 0.05  
   - 0 < X < 100
6. Visualized both actual data and predicted curve to confirm the fit.

---

## Plot Output
The figure below shows how well the predicted curve matches the actual data.

![Actual vs Predicted Curve](.parametric_curve.png)

---

## Tools Used
- Python
- NumPy
- SciPy
- Pandas
- Matplotlib

---

## Conclusion
The parameters θ = 28.1209°, M = 0.0214, and X = 54.9011 produce the best fit for the given dataset, minimizing the L1 error between predicted and actual points.
