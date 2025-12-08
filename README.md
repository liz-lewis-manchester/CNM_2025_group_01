# CNM_2025_group_01
# Input data and variables for each test cases
"""
dx is delta x
dt is delta t
"""
# Case 1
"""
From x=0 to x=20, with resolution of 0.2
5 mins=300s, so from t=0 to t=300, with resolution of 10s
initial consentration, theta =250
U = 0.1
"""
L = 20
T = 300
dx = 0.2
dt = 10
U = 10
theta = 250
variable_velocity = False

# Case 2
"""
Same model domain as case 1, but initial conditions from csv file
Should include the interpolation in the set up part with importing the file
"""
L = 20
T = 300
dx = 0.2
dt = 10{"U": 0.10, "dx": 0.2, "dt": 10.0, "label": U=0.10, dx=0.2, dt=10}
U = 10
theta = csv file after interpolation
variable_velocity = False

# Case 3
"""
compare results with different combination of U, dx, and dt, changing one per time
L and T are constant
They are saved in an array, so they can run with the same code with a for loop
"""
L = 20
T = 300
theta = 250
variable_velocity = False
configs = [ 
{"U": 0.05, "dx": 0.2, "dt": 10.0, "label": U=0.05, dx=0.2, dt=10}
{"U": 0.10, "dx": 0.2, "dt": 10.0, "label": U=0.10, dx=0.2, dt=10}
{"U": 0.10, "dx": 0.1, "dt": 10.0, "label": U=0.10, dx=0.1, dt=10}
{"U": 0.10, "dx": 0.2, "dt": 5.0, "label": U=0.10, dx=0.2, dt=5}
]

# Case 4
"""
exponentially decaying theta
rest are the same as case 1
"""
L = 20
T = 300
dx = 0.2
dt = 10
U = 10
variable_velocity = False
def exp_decay()

# Case 5
L = 20
T = 300
dx = 0.2
dt = 10
variable_velocity = True
def perturbation(degree)
