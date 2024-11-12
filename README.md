# Chatbot System Documentation

This project is a chatbot system designed to manage user and admin accounts, perform real-time data extraction, generate AI-driven responses, and support voice messaging capabilities. The system integrates various APIs, uses MongoDB for data storage, and enables efficient message routing.

---

## 1. Project Management Approach

Given the hackathon environment, we adopted a fast-paced project management approach to deliver a functional MVP:

- **Initial Planning**: Defined core features and established a minimum viable product (MVP) focused on essential functionalities.
- **Role Assignment**: Each team member took on roles based on expertise (e.g., backend, frontend, API integration).
- **Frequent Check-Ins**: Regular check-ins every few hours to synchronize progress, address blockers, and adjust tasks as needed.
- **Iterative Testing and Integration**: Continuous testing and immediate integration to quickly identify and resolve issues.
- **Final Testing and Refinement**: Conducted end-to-end testing and made final adjustments to ensure the chatbot was user-ready by the deadline.

---

## 2. Completed Features (DONE)

- **User Authentication and Account Management**: Secure login with role-based access control, distinguishing between user and admin accounts.
- **Dispatcher**: Written in Go, handles message routing, identifies new or ongoing conversations, and sends data to the Judge module.
- **Decision Engine (Judge)**: Determines the processing path for each request, routing messages to:
  - **Scraping Module** for real-time data extraction.
  - **OpenAI API** for AI-driven responses.
  - **Simple API** for straightforward responses.
  - Manages MongoDB interactions to retrieve or update conversation data.
- **Scraping Module**: Fetches real-time data from external sources as needed for user queries.
- **OpenAI API Integration**: Generates context-aware responses based on user messages.
- **Simple API**: Provides quick responses for basic queries.
- **MongoDB Database**: Stores user accounts, conversation histories, and message data to ensure continuity in interactions.
- **Voice Messaging**: Allows users to send and receive voice messages, converting audio to text for processing and text responses back into audio as needed.

---

## 3. Technology Stack by Feature

- **User Authentication and Account Management**  
  - **Technologies**: NestJS, JWT, MongoDB
  - **Description**: NestJS framework manages user authentication, leveraging JWT for secure session management and MongoDB for data storage.

- **Frontend Interface**  
  - **Technologies**: Angular
  - **Description**: The user interface is built using Angular, providing a responsive and dynamic frontend for user and admin interactions.

- **Dispatcher**  
  - **Technologies**: Go, REST API
  - **Description**: Built in Go, the Dispatcher handles message routing and interacts with the Judge module via REST API calls.

- **Decision Engine (Judge)**  
  - **Technologies**: Go, JSON, HTTP server
  - **Description**: The Judge module, written in Go, processes requests based on message type and directs them to the appropriate module, also managing MongoDB interactions.

- **Scraping Module**  
  - **Technologies**: Flask, Requests (Python)
  - **Description**: Flask is used to manage the scraping service, utilizing Requests to fetch data from external sources in response to user queries.

- **OpenAI API Integration**  
  - **Technologies**: OpenAI API
  - **Description**: Integrates with OpenAI API to generate AI-powered responses for complex user queries.

- **Simple API**  
  - **Technologies**: NestJS
  - **Description**: A lightweight API built in NestJS for handling simple queries that require minimal processing.

- **MongoDB Database**  
  - **Technologies**: MongoDB, Mongoose
  - **Description**: MongoDB is used to store user data, conversation histories, and messages, while Mongoose simplifies data modeling.

- **Voice Messaging**  
  - **Description**: Allows users to send voice messages, transcribes audio to text for processing, and converts text responses back into audio for seamless voice-based interactions.

---

This README provides a concise overview of the project management approach, completed features, and the technology stack used to build an efficient and user-friendly chatbot system with voice messaging capabilities.
