# Terminal To-Do List Application (Java)

## Overview

Terminal To-Do List is a menu-driven Java command-line application designed to help users manage their daily tasks. The application allows users to create, view, search, update, add, and delete task records while maintaining the data persistently using Java object serialization and a binary data file named `todo.dat`.

The project demonstrates the use of Java programming concepts including classes and objects, collections, file handling, object serialization, input validation, exception handling, and modular methods.

---

## Features

- Create a new task list
- Add new tasks
- Display all stored tasks
- Search tasks by serial number
- Search tasks by date
- Update existing tasks
- Delete tasks
- Maintain task completion status
- Persistent storage using `todo.dat`
- Input validation
- Error handling for invalid input and file operations
- Formatted terminal table for displaying task records
- Menu-driven command-line interface

---

## Task Data Model

Each task record contains the following fields:

| Field | Description |
|---|---|
| S.No | Unique serial number of the task |
| Hour | Scheduled hour for the task |
| Day | Day of the task |
| Month | Month of the task |
| Year | Year of the task |
| Completed | Completion status (`true`/`false`) |
| Task Description | Description of the task |

---

## Functionalities

### `createfile()`

Initializes a new binary data file named `todo.dat` or resets the existing file. The method prompts the user for the number of tasks and performs input validation before storing the records.

### `displaying()`

Reads all task records from `todo.dat` and displays them in a formatted terminal table containing the task serial number, time, date, completion status, and task description.

### `searching()`

Allows users to search for tasks using two search modes:

- Search by Serial Number (`sno`)
- Search by Date (`day`, `month`, `year`)

### `updating()`

Allows users to modify an existing task. The user can update task details and completion status while retaining existing values when appropriate.

### `deleting()`

Allows users to remove an existing task from the stored task records after selecting its serial number.

### `adding()`

Adds a new task to the existing task records with automatically generated serial numbering and input validation.

### `menu()`

Provides the main menu and controls navigation between the different task management operations.

---

## Technologies Used

The project is built using standard Java SE libraries and does not require third-party dependencies.

### Java Libraries and Concepts

- `java.io.Serializable` - Allows `TaskRecord` objects to be serialized and stored.
- `ObjectOutputStream` - Writes task objects to the binary data file.
- `ObjectInputStream` - Reads task objects from the binary data file.
- `FileInputStream` - Provides input from the stored file.
- `FileOutputStream` - Provides output to the stored file.
- `java.util.Scanner` - Reads user input from the terminal.
- `java.util.List` and `java.util.ArrayList` - Store and manage task records in memory.
- `Thread.sleep()` - Provides short pauses during selected terminal operations.
- Exception handling - Handles file-related and input-related errors.
- Input validation - Ensures that entered task information follows the expected format and boundaries.

---

## Data Storage

Task information is stored persistently in a binary file named:

```text
todo.dat

## Author

**Aanjneya Singh**  
 
B.Tech Computer Science and Engineering (Artificial Intelligence and Machine Learning)
