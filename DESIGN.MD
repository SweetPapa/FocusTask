# FocusFirst: Technical Design Document

## Overview

This technical design document provides a detailed view of the architecture and components of the FocusFirst app, as laid out in the requirements and specifications.

## 1. Vue Pages

### 1.1. DashboardPage

**Description**: The main page displaying the current 3 active tasks.

**Components Used**: 
- TaskComponent (multiple instances)
- AddTaskComponent

### 1.2. SwapReviewPage

**Description**: A page to review all the tasks swapped out before completion, along with reasons and timestamps.

**Components Used**: 
- TaskSwapReviewComponent

### 1.3. TaskHistoryPage

**Description**: A page showing a list of all tasks users have completed in the past.

**Components Used**: 
- TaskHistoryComponent

### 1.4. StatisticsPage

**Description**: A page displaying various task-related statistics.

**Components Used**: 
- StatisticsComponent

## 2. Components

### 2.1. TaskComponent

**Variables**:
- `task: Task` (Props) - The task object.

**Methods**:
- `completeTask()`: Marks the task as completed.
- `initiateSwap()`: Initiates the task swap process.

### 2.2. AddTaskComponent

**Variables**:
- `taskTitle: string` - Title of the new task.
- `taskDescription: string` - Description of the new task.

**Methods**:
- `addTask()`: Adds a new task.

### 2.3. SwapNoteComponent

**Variables**:
- `swapReason: string` - Reason for swapping out the task.

**Methods**:
- `confirmSwap()`: Confirms the task swap and logs the reason.

### 2.4. TaskSwapReviewComponent

**Variables**:
- `swapRecords: SwapRecord[]` - List of all swap records.

### 2.5. TaskHistoryComponent

**Variables**:
- `completedTasks: Task[]` - List of all completed tasks.

### 2.6. StatisticsComponent

**Variables**:
- `completedCount: number` - Number of tasks completed.
- `swapCount: number` - Number of tasks swapped out before completion.

## 3. TypeScript Definitions

### 3.1. Types

```typescript
type Task = {
    id: string;
    title: string;
    description: string;
    timestamp: Date;
};

type SwapRecord = {
    taskId: string;
    reason: string;
    timestamp: Date;
};
```

### 3.2. State Management (Vuex or Composition API)

Assuming Vuex for global state management:

```typescript
// State
state: {
    activeTasks: Task[];
    completedTasks: Task[];
    swapRecords: SwapRecord[];
},

// Mutations
mutations: {
    addTask(state, task: Task): void;
    completeTask(state, taskId: string): void;
    addSwapRecord(state, swapRecord: SwapRecord): void;
},

// Actions
actions: {
    addNewTask(context, task: Task): void;
    markTaskAsCompleted(context, taskId: string): void;
    swapOutTask(context, {taskId, reason}): void;
},

// Getters
getters: {
    activeTaskCount(state): number;
    completedTaskCount(state): number;
    swapRecordCount(state): number;
}
```

## 4. Storage

### 4.1. Local Storage or IndexedDB

For persisting tasks and swap records. 

**Keys**:
- `activeTasks`: Stores the active tasks.
- `completedTasks`: Stores the completed tasks.
- `swapRecords`: Stores the swap records.
