# Website Summarizer Project

This project consists of multiple microservices, including Java Spring Boot, Scala, Python, and PostgreSQL, to create a website summarizer. The services are containerized using Docker and can be orchestrated using Kubernetes or Docker Compose. The goal of this project is to allow users to submit a URL (such as a LinkedIn or any website), which will be crawled, summarized using an AI service, and stored in a PostgreSQL database.
## Architecture
![image](https://github.com/user-attachments/assets/0c866ef3-c6ef-4ae8-ab30-f07b18927087) <br>
## Project Overview

This project is divided into four primary components:

1. **Backend (Java Spring Boot)**  
   - A RESTful API service built with Spring Boot.
   - Handles API requests and communicates with the Scala library to process and summarize data.
   - Utilizes Gradle for building and dependency management.
   - Connects to the PostgreSQL database to log the request history.

2. **Scala Service**  
   - A library used by the Java Spring Boot backend.
   - Contains the business logic for web scraping and data processing.
   - Written in Scala and managed with Gradle.

3. **Python Service (FastAPI)**  
   - A FastAPI-based service that communicates with OpenAI or other LLM endpoints.
   - Handles content summarization and returns the summarized text.

4. **Frontend (React)**  
   - A simple React-based web application that allows users to submit a URL.
   - Displays a history of all the previous requests and their summaries.

5. **PostgreSQL Database**  
   - A PostgreSQL database is used to store all the request histories, including URLs, summaries, and timestamps.

---

## Features

- **Website Summarization**:  
  The user can submit a URL (LinkedIn or any website), and the system will summarize the content using AI-based models.
  
- **History Page**:  
  Displays a history of all previous summaries with their timestamps.

---

## Technologies

- **Backend**: Java Spring Boot, Gradle
- **Scala**: Business logic for web scraping and processing
- **Python**: FastAPI for summarization using OpenAI or other LLM APIs
- **Frontend**: ReactJS for user interface
- **Database**: PostgreSQL
- **Containerization**: Docker
- **Orchestration**: Kubernetes or Docker Compose (for local or cloud-based deployments)

---

## Prerequisites

To run this project, make sure you have the following installed on your local machine:

- Docker
- Docker Compose (optional for local deployments)
- Kubernetes (optional for cloud-based deployments)
- Minikube (if using local Kubernetes)
- Helm (for Helm chart deployments)

---

## Getting Started

### Run Commands:

- **Python server** : 
```bash
uvicorn main:app --reload
```
- **Springboot server** : 
Run from Intellij 

- **React App** : 
```bash
npm start
