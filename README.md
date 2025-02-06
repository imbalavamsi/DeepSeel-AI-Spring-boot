# Spring Boot AI Chat API with Ollama

This is a simple Spring Boot application that integrates with **Ollama AI** to generate responses using AI models. The application provides REST APIs to interact with the AI model running locally.

## Features
- Exposes REST endpoints for AI-based text generation.
- Supports both single-response (`/ai/generate`) and streaming response (`/ai/generateStream`).
- Uses **Spring AI Ollama** for AI interactions.

## Prerequisites
- **Java 17+** (Ensure Java is installed)
- **Maven** (for dependency management)
- **Spring Boot**
- **Ollama** running locally ([Install Ollama](https://ollama.ai/))

## Installation & Setup

### Clone the Repository
```sh
git clone https://github.com/imbalavamsi/DeepSeel-AI-Spring-boot.git
```

### Build the Project
```sh
mvn clean install
```

### Run the Application
```sh
mvn spring-boot:run
```

The application should start on **http://localhost:8080**.

## API Endpoints

### 1. Generate AI Response (Single Message)
- **Endpoint:** `GET /ai/generate`
- **Query Parameter:** `message` (default: `"Tell me a joke"`)
- **Example Request:**
  ```
  GET http://localhost:8080/ai/generate?message=Hello
  ```
- **Example Response:**
  ```json
  {
    "generation": "Hello! How can I assist you today?"
  }
  ```

### 2. Generate AI Response (Streaming)
- **Endpoint:** `GET /ai/generateStream`
- **Query Parameter:** `message` (default: `"Tell me a joke"`)
- **Example Request:**
  ```
  GET http://localhost:8080/ai/generateStream?message=Tell me a joke
  ```
- **Response:** A continuous Flux stream of AI responses.


## Notes
- Ensure **Ollama** is running on your local machine before testing the API.
- You can modify `ChatController.java` to enhance AI interactions.

## Author
**Bala Vamsi Maragani**  
Software Development Engineer | Java | Spring Boot | AI | Cloud | Microservices
