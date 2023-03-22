
The AirBnB Clone Project
Project Description

This is the first part of the AirBnB clone project where i worked on the backend of the project whiles interfacing it with a console application with the help of the cmd module in python.

Data (python objects) generated are stored in a json file and can be accessed with the help of the json module in python

DESCRIPTION OF THE COMMAND INTERPRETER:
The interface of the application is just like the Bash shell except that this has a limited number of accepted commands that were solely defined for the purposes of the usage of the AirBnB website
This command line interpreter serves as the frontend of the web app where users can interact with the backend which was developed with python OOP programming

Some of the commands available are:
1. Show
2. create
3. update
4. destroy
5. count

And as part of the implementation of the command line interpreter coupled with the backend and file storage system, the folowing actions can be performed:
a. Creating a new objects(ex: a new user or a new Place)
b. Retrievingan objectfrom a file, database etc
c. Doing operations on object(count, compute stats, etc ...)
d. Updating attributes of an object
e. Destroying an object

HOW TO START IT
These instructions will get a copy of the project up and running on your local machine (sandbox) for development and testing purposes.

INSTALLING
Clone the Repository of the project from Github. This will contain the simple shell programand all of its dependencies.

command: https://github.com/Nwodothomas/AirBnB_clone.git

After cloning the repository you will have a folder called AirBnB_clone. In here there will be several files that allow the program to work.

/console.py : The main executable of the project, the command interpreter.

models/engine/file_storage.py: Class that serializes instances to a JSON file and deserializes JSON file to instances

models/__ init __.py: A unique FileStorage instance for the application

models/base_model.py: Class that defines all common attributes/methods for other classes.

models/user.py: User class that inherits from BaseModel

models/state.py: State class that inherits from BaseModel

models/city.py: City class that inherits from BaseModel

models/amenity.py: Amenity class that inherits from BaseModel

models/place.py: Place class that inherits from BaseModel

models/review.py: Review class that inherits from BaseModel

How to use it
It can work in two different modes:
Interactive and Non-interactive.

In Interactive mode, the console will display a prompt (hbnb) indicating that the user can write and execute a command. After the command is run, the prompt will appear again a wait for a new command. This can go indefinitely as long as the user does not exit the program

$ ./console.py
(hbnb) help

Documented commands (type help <topic>):
========================================
EOF  help  quit

(hbnb) 
(hbnb) 
(hbnb) quit
$



In Non-interactive mode, the shell will need to be run with a command input piped into its execution so that the command is run as soon as the Shell starts. In this mode no prompt will appear, and no further input will be expected from the user.

$ echo "help" | ./console.py
(hbnb)

Documented commands (type help <topic>):
========================================
EOF  help  quit
(hbnb) 
$
$ cat test_help
help
$
$ cat test_help | ./console.py
(hbnb)

Documented commands (type help <topic>):
========================================
EOF  help  quit
(hbnb) 
$


Format of Command Input

In order to give commands to the console, these will need to be piped through an echo in case of Non-interactive mode.

In Interactive Mode the commands will need to be written with a keyboard when the prompt appears and will be recognized when an enter key is pressed (new line). As soon as this happens, the console will attempt to execute the command through several means or will show an error message if the command didn't run successfully. In this mode, the console can be exited using the CTRL + D combination, CTRL + C, or the command quit or EOF.

Arguments

Most commands have several options or arguments that can be used when executing the program. In order for the Shell to recognize those parameters, the user must separate everything with spaces.

Example:

user@ubuntu:~/AirBnB$ ./console.py
(hbnb) create BaseModel
49faff9a-6318-451f-87b6-910505c55907
user@ubuntu:~/AirBnB$ ./console.py

OR

user@ubuntu:~/AirBnB$ ./console.py $ echo "create BaseModel" | ./console.py
(hbnb)
e37ebcd3-f8e1-4c1f-8095-7a019070b1fa
(hbnb)
user@ubuntu:~/AirBnB$ ./console.py

Available commands and what they do
The recognizable commands by the interpreter are the following:

COMMAND                            DESCRIPTION

quit or EOF                         Exits the program

Usage                               By itsef

-----                               ------

help                                Provides a text describing how to use a co                                    command
Usage                               By itself -- or -- help <command>
----                                ----

create                             Create a new instance of a valid Class, save                                    it(to The JSON file) and prints the id. 
                                   Valid Classes are : BaseModel, User, State,                                   City, Amenity, Place , Reveiw.
usage                              create <class name>
-----                              -------

show                               Prints the string representation of an ins                                   ace, based on the class name and id
usage                              show <class name> <id> --or-- <class namd>.sh                                   ow(<id>)
-----                              -----

destroy                            Deletes an instance based on the class name 
                                   and id (saves the change into a JSON file)
usage                              destroy <class name> <id> --or -- .destroy
----                               ----

all                                prints all string represntation of all instan                                   ce based or not on the class name
usage                              By itself or all <class name> --or--
                                   <class name>.all()
----                               ----
update                             Updates an instance based on the class name
                                   and id by adding or updating attribute(save
                                   the changes into JSON file)
Usage                              update <class name> <id> <attribute name> " 
                                   <attribute value>" -- or -- <class name>.<up
                                   date(<id>, <attribute name>,<attribute value>                                   )--or -- <lass name>.update(<id>,<dictionary                                    representation>)
----                               ----

count                              Retrieve the number of instances of a class.

usage                              <class name>.count()


AUTHOR`
NWODO THOMAS IFEANYI | Email: Nwodothomas@gmail.com

