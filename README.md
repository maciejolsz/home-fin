# Personal Finance Dashboard Documentation

## Overview
The Personal Finance Dashboard is a web application designed to help users manage their finances effectively. It allows users to track their income, regular 
costs, and irregular expenses while providing visual representations of their financial data through charts and tables. The application is built using React, 
TypeScript, TanStack Query, and Tailwind CSS, with data stored in a local database.

## Features
1. **Dashboard Overview**:
   - Displays key financial metrics, including total income, total regular costs, total irregular expenses, and remaining budget.
   - Visual representations of data through graphs and charts.

2. **Settings Page**:
   - Allows users to input their monthly income.
   - Provides options to update or delete income information.

3. **Regular Costs Manager**:
   - A calendar view for managing regular costs (e.g., mortgage, phone bills, online services).
   - An "Add Expense" button that opens a modal form for entering regular expenses.
   - Form fields include:
     - Name (e.g., "Mortgage")
     - Amount
     - Currency
     - Description (optional)
     - Day of the month the expense is paid

4. **Irregular Expenses Manager**:
   - A form for adding irregular expenses (e.g., shopping, car maintenance, insurance).
   - Users can select the category, month, and year for the expense.
   - The form is accessible via a modal popup on the dashboard.
   - Once saved, the dashboard refreshes to reflect the new data.

## Technologies Used
- **React**: For building the user interface.
- **TypeScript**: For type safety and better development experience.
- **TanStack Query**: For data fetching and state management.
- **Tailwind CSS**: For styling the application.
- **Local Database**: For storing user data locally (e.g., using IndexedDB or LocalStorage).

## Installation
1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd personal-finance-dashboard
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Start the development server:
   ```bash
   npm start
   ```

## Application Structure
/src
├── components
│ ├── Dashboard.tsx
│ ├── Settings.tsx
│ ├── RegularCostsManager.tsx
│ ├── IrregularExpensesManager.tsx
│ ├── Modal.tsx
│ └── Chart.tsx
├── hooks
│ └── useExpenses.ts
├── context
│ └── FinanceContext.tsx
├── utils
│ └── api.ts
├── App.tsx
└── index.tsx


## Components
### 1. Dashboard
- Displays an overview of financial data.
- Integrates charts and tables to visualize income, regular costs, and irregular expenses.

### 2. Settings
- Contains a form for entering and updating monthly income.

### 3. Regular Costs Manager
- Displays a calendar view for regular costs.
- Includes an "Add Expense" button that triggers a modal form.

### 4. Irregular Expenses Manager
- Provides a form for adding irregular expenses.
- Allows users to select the category, month, and year.

### 5. Modal
- A reusable component for displaying forms in a modal popup.

### 6. Chart
- A reusable component for rendering charts using a charting library (e.g., Chart.js or Recharts).

## State Management
- Use TanStack Query to manage data fetching and caching.
- Create a custom hook (`useExpenses.ts`) to handle API calls for expenses and income.

## Local Database
- Use a local database solution (e.g., IndexedDB or LocalStorage) to store user data.
- Implement functions in `utils/api.ts` to handle CRUD operations for expenses and income.

## User Flow
1. **User visits the dashboard**: The dashboard displays an overview of their finances.
2. **User sets monthly income**: The user navigates to the settings page to input their monthly income.
3. **User manages regular costs**: The user views the calendar and adds regular costs using the modal form.
4. **User adds irregular expenses**: The user opens the modal on the dashboard to add irregular expenses.
5. **Dashboard updates**: After adding expenses, the dashboard refreshes to show the updated financial data.

## Conclusion
The Personal Finance Dashboard is a powerful tool for managing personal finances. By leveraging modern web technologies, it provides a user-friendly interface 
and valuable insights into financial health. This documentation serves as a guide for developers and users to understand the application's structure, features, 
and usage.
