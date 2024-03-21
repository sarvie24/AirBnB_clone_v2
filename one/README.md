Project: AirBnB Replica
AirBnB Logo

Project Overview
This marks the initial phase of the AirBnB replica project, focusing on backend development integrated with a console application built using the cmd module in Python. Generated data (Python objects) are stored in a JSON file and accessed using Python's json module.

Command Interpreter Overview
The command-line interface mimics the Bash shell but with a limited set of commands tailored for AirBnB website functionality. Serving as the frontend, users interact with the Python OOP backend through this interpreter.

Key commands include:

show
create
update
destroy
count
Implemented actions within the command-line interface include:

Creating new objects (e.g., User, Place)
Retrieving objects
Performing operations on objects (e.g., counting, computing stats)
Updating object attributes
Deleting objects
Getting Started
Follow these steps to set up the project locally on a Linux distribution for development and testing.

File Descriptions:
console.py: Main executable for the project, serving as the command interpreter.
models/engine/file_storage.py: Class handling serialization of instances to JSON file and deserialization from JSON to instances.
models/__ init __.py: Initializes a unique FileStorage instance for the application.
models/base_model.py: Defines common attributes/methods for other classes.
models/user.py: User class inheriting from BaseModel.
models/state.py: State class inheriting from BaseModel.
models/city.py: City class inheriting from BaseModel.
models/amenity.py: Amenity class inheriting from BaseModel.
models/place.py: Place class inheriting from BaseModel.
models/review.py: Review class inheriting from BaseModel.
Usage
The program operates in two modes: Interactive and Non-interactive.

Interactive Mode: Allows users to input commands directly into the console, with a prompt (hbnb) awaiting further commands after execution.
Non-interactive Mode: Commands are piped into the shell's execution, immediately running the provided command without displaying a prompt.
Command Input Format
Commands must be piped through an echo in Non-interactive mode. In Interactive Mode, commands are entered via keyboard, recognized upon pressing the enter key.

Command Syntax and Arguments
Commands accept various options or arguments separated by spaces.

Example:

shell
Copy code
$ ./console.py
(hbnb) create BaseModel
49faff9a-6318-451f-87b6-910505c55907
or

shell
Copy code
$ echo "create BaseModel" | ./console.py
(hbnb)
e37ebcd3-f8e1-4c1f-8095-7a019070b1fa
(hbnb)
Available Commands
Here's a summary of the recognizable commands and their functionalities:

Command	Description
quit or EOF	Exits the program
help	Provides guidance on command usage
create	Creates a new instance of a valid class and saves it to the JSON file
show	Prints the string representation of a specified instance
destroy	Deletes a specified instance
all	Prints string representations of all instances or those of a specified class
update	Updates an instance's attribute
count	Retrieves the number of instances of a class
