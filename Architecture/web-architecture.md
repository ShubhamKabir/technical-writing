# How a Web Application Works (Client–Server Architecture)

## 1. Overview

At its core, the web operates on a Request-Response cycle. This architecture divides tasks between the "Client," which requests information or services, and the "Server," which provides them. This separation allows for centralized data management and a consistent experience across different user devices.

## 2. The Client Layer

The client is the user-facing side of the application.

* Examples: Web browsers (Chrome, Safari), mobile apps, or IoT devices.

* Responsibility: It handles the User Interface (UI) and User Experience (UX). When you click a button or enter a URL, the client translates that action into an HTTP Request.

## 3. The Server Layer

The server is a powerful computer (or a cluster of them) that "serves" the needs of the client.

* Examples: Cloud servers (AWS, Google Cloud), local servers, or "Serverless" functions.

* Responsibility: It listens for incoming requests, processes logic (like checking a password), communicates with a database, and sends back an HTTP Response.

## 4. The Request-Response Cycle

1. Request: The Client sends a message (e.g., "Give me the homepage").

2. Processing: The Server receives the message, runs the necessary code, and fetches data.

3. Response: The Server sends back a message containing the requested data (HTML, CSS, JS, or JSON) along with a status code (e.g., 200 OK).