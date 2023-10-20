Certainly! Here's a `README.md` file for the FocusFirst app:

---

# FocusFirst (FocusTask): TODO List App

FocusFirst (a.k.a FocusTask) is a unique TODO list application designed to help users prioritize and concentrate on their most important tasks. By limiting users to three tasks at a time, the app ensures a focused approach. Swapping tasks requires a conscious decision, and the app logs these decisions for future reflection.

## Table of Contents

- [Features](#features)
- [How It Works](#how-it-works)
- [Technical Specifications](#technical-specifications)
- [Project Structure](#project-structure)
- [Development](#development)

## Features

1. **Task Management**: Add, view, and complete tasks.
2. **Focus Mode**: Limit of 3 active tasks at any given moment.
3. **Swap Reasoning**: Before swapping out an active task for a new one, provide a reason.
4. **Review Decisions**: Review all swapped tasks, the reasons provided, and the time of the swap.
5. **Statistics**: View how many tasks you've completed and how often you swap tasks.

## How It Works

1. **Dashboard**: The main interface displays your current 3 active tasks. Here, you can mark tasks as completed or initiate a task swap.
2. **Add Task**: If you have fewer than 3 tasks, you can add a new one to your list.
3. **Swap Task**: If you want to replace an active task, click on the swap button. You'll be prompted to provide a reason for the swap.
4. **Review Swaps**: Navigate to the review section to see all your swapped tasks, the reasons for each swap, and the timestamp of the action.
5. **Task History**: View a list of all your completed tasks.
6. **Statistics**: See an overview of your task management behavior.

## Technical Specifications

- **Frontend Framework**: Quasar (with Vue 3)
- **Programming Language**: TypeScript
- **Platform Wrapper**: Capacitor
- **State Management**: Vuex (or Composition API)
- **Storage**: Local Storage or IndexedDB

## Project Structure

- `src/pages/`: Contains all Vue pages like DashboardPage, SwapReviewPage, etc.
- `src/components/`: Houses reusable Vue components like TaskComponent, AddTaskComponent, etc.
- `src/store/`: State management with Vuex (or Composition API) for tasks and swap records.
- `src/types/`: TypeScript definitions and types.
- `src/assets/`: Static assets like images, fonts, etc.
- `public/`: Public assets and `index.html`.

## Development

To set up the project locally:

1. Clone the repository.
2. Install dependencies using `npm install`.
3. Run the development server with `quasar dev`.
4. Build for production with `quasar build`.

For more detailed setup and development guidelines, please refer to Quasar's official documentation.
