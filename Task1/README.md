# Bresenham's Line Drawing Algorithm


The Bresenham line drawing algorithm is a method used to draw a straight line between two points on a grid. It operates by selecting which pixels to activate to approximate the line. The algorithm calculates the slope of the line and then iteratively determines which pixel to activate next, based on the relative positions of neighboring pixels and the ideal line. It utilizes integer arithmetic and an error term to efficiently compute the line without the need for floating-point calculations. The algorithm maintains precision and performance by minimizing computational overhead and adapting to draw lines in various directions and orientations within the grid.


## Code Review in Detailed 

**Objective:** The code aims to implement the Bresenham line drawing algorithm to generate intermediate points between two given points and visualize them using matplotlib.

**Function "Input Parameters":** 
- Extracts x and y coordinates from a list of points.
- Calculates grid dimensions based on the maximum x and y coordinates.
- Creates a grid of pixels using NumPy.
- Fills the cells corresponding to (x, y) coordinates with value 1.
- Plots the grid using matplotlib, adjusting figure size, colormap, origin, extent, transparency, and aspect ratio.
- Adds labels for axes and a title to the plot.
- Improves grid lines for better visibility.
- Displays the plot.

**Function "slope_less_than_one":** 
- Computes intermediate points between two given points with a slope less than one using the Bresenham algorithm.
- Initializes lists to store intermediate points and decision parameters.
- Determines starting point, change in y and x, and decision parameter.
- Iterates over x coordinates, updating decision parameter and y coordinate as needed.
- Prints intermediate points and decision parameters.
- Calls *visualize_points* to visualize the intermediate points.

**Function "slope_greater_than_one":**
- Computes intermediate points between two given points with a slope greater or equal to one using the Bresenham algorithm.
- Initializes lists to store intermediate points and decision parameters.
- Determines starting point, change in y and x, and decision parameter.
- Iterates over y coordinates, updating decision parameter and x coordinate as needed.
- Prints intermediate points and decision parameters.
- Calls visualize_points to visualize the intermediate points.

**Function "bresenham_line":**

- Unpacks coordinates of two given points.
- Calculates change in y and x.
- Determines whether slope is less than one or greater/equal to one and calls corresponding functions accordingly.

**Visualization:**

- For each pair of given points, the intermediate points are computed using the Bresenham algorithm and visualized on a grid.
- The plot shows the grid with filled cells at the intermediate points between the given points.

Output:

- Displays the given points, indicates the slope condition, prints intermediate points, decision parameters, and visualizes the points on a grid for each pair of points provided.


## Algorithm Link

 - [Bresenham's Line Drawing in Jupyter Notebook](https://github.com/Jisan10667/Computer-Graphics-And-Image-Processing-Lab-Works-/blob/main/Task1/Bressenham_Line_Drawing_ALgorithm.ipynb)
