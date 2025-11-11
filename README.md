# AI Cabin Price Predictor

Final project for the Building AI course  
by Mohamed Ahmed Hassan

## Your idea in a nutshell
The AI Cabin Price Predictor is a machine learning–based tool that estimates the price of a cabin based on its characteristics...


The AI Cabin Price Predictor is a machine learning–based tool that estimates the price of a cabin based on its characteristics — such as size, sauna size, distance to a lake, number of bathrooms, and proximity to neighbors.
It demonstrates how artificial intelligence can learn relationships between property features and prices to support fair, data-driven pricing decisions.

Background

Determining fair property prices is a common challenge in real estate markets, especially for cabins and countryside homes where values depend on several environmental and structural factors. Sellers often rely on intuition, while buyers lack accurate tools to compare options.

This project addresses the need for automated, transparent price estimation by using AI to model the relationship between cabin features and their selling prices.

Why this matters

Property pricing errors can cause financial losses for both buyers and sellers.

Manual estimation methods are subjective and inconsistent.

AI brings data-driven fairness, speed, and transparency.

Personal motivation

I chose this idea because it connects what I learned about regression, neural networks, and data analysis in the Building AI course. It’s a simple but practical use case that demonstrates how machine learning can solve real-world problems — and it’s directly inspired by exercises from the course.

Data and AI techniques
Data sources

The project uses synthetic data similar to the cabin dataset provided in the course examples. Each record includes:

Size of cabin (m²)

Size of sauna (m²)

Distance to lake (m)

Number of indoor bathrooms

Proximity of neighbors (m)

Cabin price (in euros)

Example dataset:

size | sauna | distance | bathrooms | neighbors | price
--------------------------------------------------------
25   | 2     | 50       | 1         | 500       | 127900
82   | 5     | 20       | 2         | 120       | 268000
130  | 6     | 10       | 2         | 600       | 460700

AI methods used

Linear Regression — to model the linear relationship between features and prices.

Neural Network (2 hidden layers) — for more complex non-linear dependencies.

k-Nearest Neighbors (kNN) — for comparison with simpler distance-based prediction.

NumPy and Scikit-learn — for data processing, fitting, and evaluation.

Code
from sklearn.linear_model import LinearRegression
import numpy as np

X = np.array([[25, 2, 50, 1, 500],
              [82, 5, 20, 2, 120],
              [130, 6, 10, 2, 600]])
y = np.array([127900, 268000, 460700])

model = LinearRegression().fit(X, y)
price = model.predict([[82, 2, 65, 3, 516]])
print("Predicted price:", price)
