# chat-app
Chat App

This project implements a two-way network chat using Spring Boot and WebSocket. Users can connect to a chat room, send and receive messages in real-time.

Features
Real-time two-way communication using WebSocket.
Simple, responsive UI for chat.
Lightweight and fast with Spring Boot.
Prerequisites
Before running the application, ensure you have the following installed on your machine:

Java Development Kit (JDK) (Version 8 or higher)
Maven (Build tool)
A web browser (e.g., Chrome, Firefox)
Project Structure
plaintext
Copy code
chat-app/
├── src/main/java/com/example/chatapp
│   ├── ChatAppApplication.java       # Main Application Class
│   ├── config
│   │   └── WebSocketConfig.java      # WebSocket Configuration
│   ├── controller
│   │   └── ChatController.java       # Controller for Chat Functionality
│   ├── model
│   │   └── ChatMessage.java          # Model for Chat Messages
│   ├── service
│   │   └── MessageHandlerService.java # Service for Message Processing
├── src/main/resources
│   ├── application.properties        # Application Configuration
│   ├── static
│   │   ├── index.html                # Chat UI HTML File
│   │   ├── chat.js                   # Chat UI JavaScript File
│   │   └── chat.css                  # Chat UI CSS File
└── pom.xml                           # Maven Configuration
Getting Started
1. Clone the Repository
bash
Copy code
git clone https://github.com/your-username/chat-app.git
cd chat-app
2. Build the Application
Run the following command to build the project:

bash
Copy code
mvn clean install
3. Run the Application
Start the Spring Boot application using:

bash
Copy code
mvn spring-boot:run
Or, if you prefer to use the JAR file:

bash
Copy code
java -jar target/chat-app-1.0-SNAPSHOT.jar
4. Access the Chat UI
Open your browser.
Go to: http://localhost:8080.
Open the same URL in another browser tab or window to simulate a two-user chat.
Configuration
Change the Port
By default, the application runs on port 8080. To change this:

Open src/main/resources/application.properties.
Modify the port configuration:
properties
Copy code
server.port=8081
Troubleshooting
Common Issues
Whitelabel Error Page (404):

Ensure index.html is in the src/main/resources/static directory.
Restart the application after making changes.
WebSocket Not Connecting:

Check the browser console for errors.
Ensure the server is running without issues.
Port Already in Use:

Change the port in application.properties.
Technologies Used
Spring Boot: Backend Framework
WebSocket: Real-time communication protocol
HTML/CSS/JavaScript: Frontend
SockJS and Stomp.js: WebSocket libraries for frontend
Future Improvements
Add user authentication.
Store chat messages in a database.
Allow private messaging between users.
