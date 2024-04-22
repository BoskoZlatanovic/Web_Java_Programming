Homework: Public Chat Application
Description

This Homework involves creating a chat application using Java sockets that allows public communication among all connected users. The system consists of a server that manages client connections and facilitates message exchanges.
Server Features

    Client Connection: The server will handle incoming connections from clients.
    Unique Identification: Upon connection, the server will prompt each new client for a unique username. No two clients can have the same username at the same time.
    Welcome Message: After a successful connection and username setup, the server will send a welcome message to the client. It will also notify all connected clients about the new connection.
    Message History: The connected client will be shown the history of the last 100 messages, including the message content, author, and timestamp. The history is maintained in the server's memory.

Messaging

    Continuous Listening: The server continuously listens for new messages from clients.
    Message Storage: Each received message is stored in the history and all connected clients are notified of the new message.
    Censored Words: The server has a predefined set of censored words. If a message contains any censored words, those words are modified so that all letters except the first and last are replaced with asterisks (*).

Client Display

    Message Format: Messages are displayed in the client console in the following format:

    php

    <Timestamp of message> - <Username of sender>: <Message content>

Error Handling

    Connection Interruption: If there is an error on the server or client, the connection will be terminated and an error message will be displayed in the console.

Code Structure

    Special attention should be given to the structure and organization of the code to ensure clarity and maintainability.
