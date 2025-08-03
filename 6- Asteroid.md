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



# Working inside the main 

## Modules
###importing
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

```

```
