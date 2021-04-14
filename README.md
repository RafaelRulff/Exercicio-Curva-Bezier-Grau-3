from Bezier import Bezier
import numpy as np

t_points = np.arange(0, 1, 0.01)
points1 = np.array([[0, 0], [0, 8], [5, 10], [9, 7], [4, 3]])
curve1 = Bezier.Curve(t_points, points1)
import matplotlib.pyplot as plt

plt.figure()
plt.plot(
	curve1[:, 0],   # x-coordinates.
	curve1[:, 1]    # y-coordinates.
)
plt.plot(
	points1[:, 0],  # x-coordinates.
	points1[:, 1],  # y-coordinates.
	'ro:'           # Styling (red, circles, dotted).
)
plt.grid()
plt.show()
