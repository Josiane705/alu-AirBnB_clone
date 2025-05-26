This is the backend foundation of an AirBnB clone. It provides a command-line interpreter to manage AirBnB objects—users, places, cities, states, amenities, and reviews—using JSON file storage for persistence.

Project Description

Goal: Build a CLI to create, retrieve, update, and delete AirBnB-like objects.

Architecture:

BaseModel: Parent class handling id, created_at, updated_at, serialization, and deserialization.

Models: Subclasses (User, State, City, Amenity, Place, Review) inherit from BaseModel.

Storage Engine: FileStorage class serializes objects to file.json and reloads them.

Console: Uses Python's cmd module to provide commands for object management.

Command Interpreter

The console (console.py) accepts the following commands at the (hbnb) prompt:

Command

Description

create <class_name>

Creates a new instance of <class_name> and prints its id.

show <class_name> <id>

Prints the string representation of an instance.

destroy <class_name> <id>

Deletes an instance based on class name and id.

all [<class_name>]

Prints all instances, or all of <class_name>, as string representations.

update <class_name> <id> <attr_name> "<value>"

Updates or adds attribute attr_name with value to an instance.

count <class_name>

(Extra) Counts the number of instances of <class_name>.

quit or EOF

Exits the console.

How to Start It

git clone https://github.com/Josiane705/alu-AirBnB_clone.git
cd alu-AirBnB_clone
chmod +x console.py models/*.py models/engine/*.py
python3 console.py

Project Requirements

Python 3.8+ on Ubuntu 20.04 LTS

All scripts start with #!/usr/bin/python3 and are executable

Code style follows PEP8 (use pycodestyle . to check)

All modules, classes, and methods include descriptive docstrings

Unit tests under tests/ using Python's unittest module

Collaboration

Use branches and pull requests on GitHub to organize team work and code reviews
