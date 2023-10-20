# TODO List App: FocusFirst

## Overview:
FocusFirst is a TODO list app designed to help users concentrate on their most essential tasks. The app's core feature is its restriction to three tasks at any time, ensuring users prioritize and stay focused. Task swapping requires users to write a note, ensuring they are conscious of their actions and the reasons behind them.

## Features:

### 1. **Add Task**:
- Users can add a new task with a title and optional description.
- Maximum of 3 tasks can be active at any time.

### 2. **View Active Tasks**:
- The main dashboard displays the current 3 active tasks.
- Each task shows its title, description, and an option to mark it as completed.

### 3. **Complete Task**:
- Users can mark a task as completed.
- Once marked, the task is removed from the active tasks list.

### 4. **Swap Task**:
- If a user wants to swap an active task with a new one, they must provide a reason for the pivot.
- This reason is saved with a timestamp for future reference.

### 5. **Review Task Swaps**:
- Users can review a list of all tasks they've swapped out before completion.
- Each entry in this list will show the task title, the timestamp of the swap, and the reason provided for the swap.

### 6. **Task History**:
- Users can see a list of all tasks they have completed.

### 7. **Statistics**:
- Display the number of tasks completed.
- Display the number of tasks swapped out before completion.


## Technical Specifications:

### **Framework & Languages**:
- **Frontend Framework**: Quasar (with Vue 3).
- **Programming Language**: TypeScript.
- **Platform Wrapper**: Capacitor.

### **Components**:

1. **Task Component**:
    - Displays the task title and description.
    - Contains buttons for completion and swapping out.

2. **Add Task Component**:
    - Input fields for task title and optional description.
    - Button to add the task.

3. **Swap Note Component**:
    - Input field for entering the swap reason.
    - Button to confirm the swap.

4. **Task Swap Review Component**:
    - Displays a list of tasks swapped out before completion with reasons and timestamps.

5. **Task History Component**:
    - Displays a list of completed tasks.

6. **Statistics Component**:
    - Displays task-related statistics.

### **Data Structure**:

1. **Task**:
    - `id`: Unique identifier.
    - `title`: Task title.
    - `description`: Optional task description.
    - `timestamp`: Creation date and time.

2. **SwapRecord**:
    - `taskId`: Task's unique identifier.
    - `reason`: Reason for the swap.
    - `timestamp`: Date and time of the swap.

### **Storage**:
- Local storage or indexedDB for storing tasks, swap records, and statistics.
