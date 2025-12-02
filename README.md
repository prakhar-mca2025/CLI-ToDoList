ToDoCLI — A Simple C++ Command-Line To-Do List Manager (Introduction)

  • A lightweight and efficient command-line To-Do List application built in C++.
  • Tasks are stored persistently using binary file storage, ensuring your tasks remain saved across program restarts.
  • This project demonstrates:
  • Object-oriented design (Task + ToDoList classes)
  • Binary file handling in C++
  • Basic menu-driven CLI interaction
  • Clean separation of concerns

Features:
 • Add Tasks
 
 Create new tasks with custom descriptions.
 (Implemented in addTask() of ToDoList.cpp 
 
 • View All Tasks
   Displays task number, description, and status (Completed / Pending).
   (Implemented in viewTasks() 
 
 • Mark Tasks as Completed
   Updates the task state and persists it.
   (Implemented in completeTask() 
 
 • Delete Tasks
   Removes tasks permanently from the list.
   (Implemented in deleteTask() 
 
 • Persistent Storage
   All tasks are saved into a binary file: tasks.dat


Project Structure:
  ToDoCLI
  │
  ├── main.cpp           # Menu-driven CLI program
  ├── Task.h             # Task model class
  ├── Task.cpp
  ├── ToDoList.h         # Manages tasks and file operations
  ├── ToDoList.cpp
  └── tasks.dat          # Auto-generated binary storage file

• Class Overview
  1. Task Class
      File: Task.h & Task.cpp
      Stores:
      • char description[100] (fixed-size, for binary safety)
      • bool completed
      Defined and implemented in Task

  2. ToDoList Class
     Handles:
       • Storing vector of tasks
       • Adding / viewing / completing / deleting
       • Saving + loading from tasks.dat
      Defined and implemented in ToDoList

main.cpp
  Runs the interactive CLI menu with:
    1. Add Task
    2. View Tasks
    3. Complete Task
    4. Delete Task
    5. Exit

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
    Automatically created on first run
    Overwritten each time tasks change
    Stores raw Task objects (fixed-size, safe for binary operations)

Future Improvements
  • Edit task descriptions
  • Add due dates or priority levels
  • Use JSON or plain text instead of binary
  • Add colorized terminal output
  • Add search or filtering
  • Export tasks to a readable file
  
