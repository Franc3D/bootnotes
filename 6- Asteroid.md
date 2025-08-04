# These are the notes I am taking for course 6 - Recreating the asteroid game

# VIRTUAL ENVIRONMENT (VENV) (using UV)
Each project may require a different working environment, in this case we want to use pygame version 2. To prevent all projects from using pygame 2 it is best to setup a virtual environment on that project.
### Initialisation
```
uv init your-project-name
cd your-project-name
```
### Create a virtual environment in root 
```
uv venv
```
### Activate the virtual environment
```
source .venv/bin/activate
```
Now the (project_name) appears at the very start of your terminal prompt
### Add the library you want to the Virtual environment
```
uv add pygame==2.6.1
```
This tells Python that this project requires pygame version 2.6.1.
### Make sure pygame is installed
```
uv run -m pygame
```
### To execute your main.py
Trying to run any .py files in the project using python3 main.py may result in errors. To execute the project in the virtual environment use the command below.
```
uv run main.py
```
CTRL + C to close



# Working inside the main 

## Modules
### Importing
In Python, each .py file is a module, and we can import functions, variables, and classes from one module into another with the import statement. The name of a module is the filename (without the .py extension).
```
# import the connect_database function
# and the database_version variable
# from database.py into the current file
from database import connect_database, database_version
```
Or if you want to import everything
```
# import everything from the module
# database.py into the current file
from database import *
```
## FPS
### Delta time
We use "delta time" to represent the amount of time that has passed since the last frame was drawn. Decoupling the game speed from the speed it's being drawn to the screen will prevent the game from running based on your processor's speed.
```
# Declare after pygame.init()
clock = pygame.time.Clock()
delta_time = 0

# Declare at the very end
dt = clock.tick(60) / 1000   
```
The .tick() method will wait the amount of time declared as 1/x seconds (60). It also stored the amount of time in seconds(in milliseconds without the / 1000) the window was active that frame (before the wait).  
## Draw player



```

```








