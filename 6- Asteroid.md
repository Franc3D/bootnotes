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

## Create the game loop
### we need to do the following multiple times a second to get a proper game loop :

    1.Check for player inputs
    2.Update the game world
    3.Draw the game to the screen
The game loop will take place inside an infinite loop to ensure the game lasts forever(until we close)
```
# Content we declare before the loop starts  

while loop
  # Content we want to show every seconds
```
### But we need a canvas if we want to draw
Using pygame we can generate a GUI window called a display, this will appear as a regular window where we can "draw" the displayable content of the game. This is to be added before the loop
```
screen = pygame.display.set_mode((SCREEN_WIDTH, SCREEN_HEIGHT))
```
Afterward, you will want to show the screen on every frames
```
# Erase what was previously displayed
screen.fill("black")

# adding all the stuff to the screen

# Display the content of the screen
pygame.display.flip()
```
## Make sure the window is closable when pressing the top right X
The game can currently only be stopped when pressing CTRL + C in the console, to allow for a more intuitive way to close the game use the following line of code at the start of the loop :
```
for event in pygame.event.get():
    if event.type == pygame.QUIT:
        return
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



## Making a player module
###for every game you will need to control something, a player class will help reach that goal
```

```








