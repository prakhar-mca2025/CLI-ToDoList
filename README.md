ToDoCLI — A Simple C++ Command-Line To-Do List Manager (Introduction)

  • A lightweight and efficient command-line To-Do List application built in C++. <br>
  • Tasks are stored persistently using binary file storage, ensuring your tasks remain saved across program restarts. <br>
  • This project demonstrates: <br>
    • Object-oriented design (Task + ToDoList classes) <br>
    • Binary file handling in C++ <br>
    • Basic menu-driven CLI interaction <br>
    • Clean separation of concerns <br>

Features:
 • Add Tasks <br>
    Create new tasks with custom descriptions. <br>
    (Implemented in addTask() of ToDoList.cpp  <br>
 
 • View All Tasks <br>
   Displays task number, description, and status (Completed / Pending). <br>
   (Implemented in viewTasks() <br>
 
 • Mark Tasks as Completed <br>
   Updates the task state and persists it. <br>
   (Implemented in completeTask()  <br>
 
 • Delete Tasks <br>
     Removes tasks permanently from the list. <br>
     (Implemented in deleteTask()  <br>
 
 • Persistent Storage <br>
   All tasks are saved into a binary file: tasks.dat <br>


Project Structure: <br>
  ToDoCLI
  │
  ├── main.cpp           # Menu-driven CLI program
  ├── Task.h             # Task model class
  ├── Task.cpp
  ├── ToDoList.h         # Manages tasks and file operations
  ├── ToDoList.cpp
  └── tasks.dat          # Auto-generated binary storage file

• Class Overview
  1. Task Class <br>
      File: Task.h & Task.cpp <br>
      Stores: <br>
      • char description[100] (fixed-size, for binary safety) <br>
      • bool completed <br>
      Defined and implemented in Task <br>

  2. ToDoList Class <br>
     Handles: <br>
       • Storing vector of tasks <br>
       • Adding / viewing / completing / deleting <br>
       • Saving + loading from tasks.dat <br>
      Defined and implemented in ToDoList <br>

main.cpp
  Runs the interactive CLI menu with:
    1. Add Task <br>
    2. View Tasks <br>
    3. Complete Task  <br>
    4. Delete Task <br>
    5. Exit  <br>

How to Compile & Run
  • Using g++
  • g++ main.cpp Task.cpp ToDoList.cpp -o todo
    ./todo
    
    
Usage Example
  --- TO DO LIST MENU ---
  1. Add Task
  2. View Tasks
  3. Complete Task
  4. Delete Task
  5. Exit
  Enter choice: 1
  Enter task description: Finish C++ project
  Task added.
  
  --- TO DO LIST MENU ---
  2. View Tasks
  
  ----- TASK LIST -----
  1. Finish C++ project [Pending]
  ----------------------

Binary File Storage:
  The app saves all tasks to:tasks.dat
    • Automatically created on first run.  <br>
    • Overwritten each time tasks change.  <br>
    • Stores raw Task objects (fixed-size, safe for binary operations). <br>

Future Improvements
  • Edit task descriptions. <br>
  • Add due dates or priority levels. <br>
  • Use JSON or plain text instead of binary.  <br>
  • Add colorized terminal output.  <br>
  • Add search or filtering.  <br>
  • Export tasks to a readable file.  <br>
  
