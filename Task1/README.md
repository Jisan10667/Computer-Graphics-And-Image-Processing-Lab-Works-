
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


## Output Images

![For 0<m<1](https://github.com/Jisan10667/Computer-Graphics-And-Image-Processing-Lab-Works-/blob/main/Task1/Output/For%200%3Cm%3C1.png)

![For m>1](https://github.com/Jisan10667/Computer-Graphics-And-Image-Processing-Lab-Works-/blob/main/Task1/Output/For%20m%3E1.png)


## Adjustments for Slope m > 1
For the slope greater than 1 scenario in the Bresenham line drawing algorithm, adjustments are necessary to ensure accurate computation of intermediate points. The standard Bresenham algorithm is designed to handle slopes with absolute values less than or equal to 1 efficiently. When the slope exceeds 1, the algorithm needs to be adapted to accommodate this specific case.

The adjustments made for the slope greater than 1 scenario include:

**Interchanging the Roles of x and y:** In the standard Bresenham algorithm, the roles of x and y are interchanged when the slope is greater than 1. This means that instead of considering the progression along the x-axis for each step, the algorithm now progresses along the y-axis.

**Incrementing y by 1:** With a slope greater than 1, incrementing y by 1 for each step ensures that the algorithm accurately traverses the line between the two points. This adjustment maintains the integrity of the line's trajectory while accounting for the steep slope.

**Updating the Decision Parameter:** The decision parameter calculation is adjusted to reflect the change in the progression direction. The decision parameter determines the next pixel to be chosen and guides the algorithm's progression. In the case of a slope greater than 1, the decision parameter is updated based on the progression along the y-axis.

**Handling the Decision Parameter Conditions:** The conditions for updating the decision parameter are adjusted to suit the new progression direction along the y-axis. This ensures that the algorithm correctly selects the next pixel while drawing the line.

By making these adjustments, the algorithm can effectively handle slopes greater than 1 and accurately compute the intermediate points along the line between the given points.





## Algorithm Link

 - [Bresenham's Line Drawing in Jupyter Notebook](https://github.com/Jisan10667/Computer-Graphics-And-Image-Processing-Lab-Works-/blob/main/Task1/Bressenham_Line_Drawing_ALgorithm.ipynb)



