# TheBugBusters (Frontend)

*This repository contains the **Frontend** source code and user interface for TheBugBusters project, developed for the Dedalus Datathon 2025. The backend logic, including the AI chatbot engine and the database management, can be found in the [Backend Repository](https://github.com/Lustom/TheBugBustersBackend).*

## Overview
This frontend application serves as the interactive layer for the clinical assistant developed during the **Dedalus Datathon 2025**. It was designed as a lightweight, high-performance Single Page Application (SPA) to provide medical staff with an intuitive tool for patient management and clinical data retrieval. 

The interface communicates seamlessly with the backend REST API through asynchronous requests, handling complex data structures, dynamic UI updates, and real-time data visualization without relying on heavy frontend frameworks.

## Core Features & Technical Implementation

### 1. Asynchronous State Management & API Integration
The application architecture relies on asynchronous JavaScript (`async/await` and Promises) to interact with the backend API. A custom state management system was implemented to handle multiple isolated chat sessions concurrently. This ensures that conversations and clinical context remain strictly tied to the currently selected patient, preventing cross-contamination of medical data. Robust error handling and retry mechanisms were also implemented for API communications.

### 2. Dynamic Data Visualization
A key feature of the interface is the ability to render complex database queries into visual formats. By integrating **Chart.js**, the frontend dynamically parses JSON payloads returned from the backend's Text-to-SQL engine and automatically constructs bar or line charts. This allows medical staff to visualize clinical trends directly within the chat interface based on natural language requests.

### 3. Client-Side PDF Generation
To facilitate medical record-keeping, a client-side reporting module was implemented using **jsPDF**. The application dynamically compiles patient metadata and the current chat history into a formatted PDF document, which can be generated and downloaded instantly without requiring server-side processing.

### 4. Session Export & Import
A custom file-handling mechanism was built using the HTML5 File API and `Blob` objects. This allows users to serialize the active chat history, export it as a `.json` file for local storage, and later re-import it to resume the session seamlessly.

### 5. Advanced UI/UX Components
The interface includes several custom-built UI components tailored for clinical environments:
* **Resizable & Collapsible Sidebar:** Implemented via native DOM mouse events to allow users to customize their workspace dimensions.
* **Real-time Search & Filtering:** A dynamic search algorithm filters the patient list instantly based on numeric IDs or text strings.
* **Theme Management:** A persistent dark/light mode toggle was integrated to reduce eye strain in different lighting conditions.

## Technologies Used
* **HTML5 & CSS3** (Responsive Layout & Styling)
* **Vanilla JavaScript / ES6+** (Core Logic, DOM Manipulation, Fetch API)
* **Chart.js** (Dynamic Data Visualization)
* **jsPDF** (Client-side PDF Generation)

## Local Setup & Installation

To run the frontend interface locally:

1. **Clone the repository** and navigate to the frontend directory.
2. **Launch the application:** Since the project uses Vanilla JS, no build steps or package managers (like `npm`) are required. Simply open the `index.html` file in any modern web browser. 
   *(Note: Using a local server extension like VS Code's "Live Server" is recommended for optimal performance).*
3. **Connect to the Backend:** Ensure the backend server is running locally on `http://127.0.0.1:5000/` for the API calls to function correctly.

<img width="1391" height="777" alt="THE BUG BUSTERS" src="https://github.com/user-attachments/assets/52a32cd7-9cb0-4a52-8a98-a1c388c2cd93" />
