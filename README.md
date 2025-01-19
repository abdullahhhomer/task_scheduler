# Task Scheduler

This Task Scheduler is a Python-based tool implemented as a Jupyter Notebook. It allows users to manage tasks effectively by performing operations such as creating, updating, deleting, and listing tasks. Tasks are stored in a JSON file (`tasks.json`) for persistence.

## Features

- **Task Creation**: Add new tasks with descriptions and statuses.
- **Task Updating**: Modify existing tasks' descriptions, statuses, or both.
- **Task Deletion**: Remove tasks by their unique IDs.
- **Status Management**: Mark tasks as "not done," "in progress," or "done."
- **Task Listing**:
  - List all tasks.
  - List tasks filtered by status (e.g., "done," "not done," or "in progress").
- **Persistent Storage**: All tasks are saved in a JSON file (`tasks.json`) and automatically updated when the program exits.

## How It Works

1. **File Handling**: The script checks for the existence of `tasks.json`. If it doesn't exist, it creates a new empty file.
2. **Task Management**:
   - Tasks are managed as a list of dictionaries, each containing:
     - `Id`: Unique identifier.
     - `description`: Task description.
     - `status`: Task status.
     - `created_at`: Timestamp of task creation.
     - `updated_at`: Timestamp of last modification.
3. **Functionality**:
   - **Add Task**: Creates a new task with user-provided details.
   - **Update Task**: Edits an existing task identified by its ID.
   - **Delete Task**: Removes a task from the list by its ID.
   - **Write to File**: Updates `tasks.json` when the program exits.
4. **Interactive Menu**: The script provides a user-friendly menu for managing tasks in a loop until the user exits.

## Functions Overview

- **`check_for_file(path_file)`**: Ensures the existence of `tasks.json`.
- **`create(description, status, data)`**: Adds a new task.
- **`update(Id, description, status, data)`**: Updates a task's details.
- **`delete(Id, data)`**: Deletes a task.
- **`write(path_file, data)`**: Writes task data to `tasks.json`.
- **`main()`**: Main loop handling user interaction and task management.

## Usage

1. Clone or download this repository.
2. Open the `task_scheduler.ipynb` file in Jupyter Notebook or Jupyter Lab.
3. Run all cells in the notebook.
4. Follow the on-screen menu to manage tasks.

## Example Menu

```
Options:
1. Add Task
2. Update Task
3. Delete Task
4. Mark Task as In Progress
5. Mark Task as Done
6. List All Tasks
7. List Done Tasks
8. List Not Done Tasks
9. List In Progress Tasks
10. Exit
```

## Dependencies

- Python 3.6+
- `json` (built-in library)
- `os` (built-in library)
- `datetime` (built-in library)

## Notes

- The program ensures tasks are saved to `tasks.json` only when exiting. Avoid abrupt termination to prevent data loss.
- Task IDs are automatically managed based on the current number of tasks.

## License

This project is open-source and available under the MIT License.

##Link 

[https://github.com/abdullahhhomer/task_scheduler](https://roadmap.sh/projects/task-tracker)
