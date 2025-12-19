# CNM_2025_group_01
## How the concentration solver code works. 

We have created a code which calulated the concentration of a pollutant along a river at various times. 

The code can be split into 4 sections: 
1. The interpolation of data from a csv file
2. the definition of the fuction to solve the equation ∂𝜃/∂𝑡 = ― 𝑈 ∂𝜃/∂𝑥 using the finite difference method 
3. the input and definition of the variables
4. plotting the results and animating the graph with relation to time

In order to run the code, the following variables have to be input into the code:
- L: Length of the river
- T: Time period
- dx: spatial resolution
- dt: time interval
- U: velocity profile
- boundary_theta: Concentration of pollutant at x = 0, when t = 0
  - if boundary_theta is a constant then the interpolation sections of the code are not required and must not be included

The base code can be found in the folder 'solver'. After all the variables have been input the code can be run to solve the quation and calculate the variation in concentration. A graph of Concentration of pollutant against position in river is plotted and shows the change with respect to time.

Examples of the code's function as specified by the test cases can be found in the folder 'tests'. 
