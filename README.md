# Java Chat System

A simple GUI-based chat application built with Java Swing that allows multiple users to communicate in real-time via a central server.

## Features

- **User Registration**: Users must register with a unique username
- **Real-time Messaging**: Instant message broadcasting to all connected clients
- **Active User List**: Displays all currently connected users
- **Connection Management**: Handles user disconnections gracefully
- **Server Monitoring**: Server admin can view all connection activities

## Components

1. **Server** (`Server.java`)
   - Manages all client connections
   - Broadcasts messages to all connected clients
   - Maintains list of active users
   - Shows connection/disconnection events

2. **Client Register** (`ClientRegister.java`)
   - Initial user interface for username registration
   - Validates username uniqueness
   - Establishes connection to server

3. **Chat Client** (`Chat.java`)
   - Main chat interface
   - Displays messages and active users
   - Handles message sending/receiving

## How to Run

### Prerequisites
- Java JDK 8 or later

### Running the System

  -Usage Instructions

  1. Server Administration

  -Launch the server application
  -View real-time connection log
  -Monitor active connections
  -Server runs until manually closed

2. Client Usage

  -Launch ClientRegister
  -Enter unique username
  -Minimum 3 characters. No special characters
  -Click "ENTER" to connect

In chat window:
  -Type messages in bottom panel
  -Click "SEND" or press Enter
  -View active users in right panel
  -Close window to disconnect

## Technical Details

Communication Protocol: 

1. Client-Server: port 2025
2. Data Format:	UTF-8 Strings	

## Thread Management

### Server:
  1. ClientAcceptThread (main thread)
  2. MsgReadThread (per client)
  3. ClientListUpdateThread

### Client:
  1. MessageReceiverThread
  2. UI Event Dispatch Thread

## Future Enhancements

#### Security:
  1. Password authentication
  2. Message encryption
  3. IP filtering

### Features:
  1. File sharing
  2. Message history
  3. Emoji support

### Performance:
  1. Connection pooling
  2. Message compression

### UI Improvements:
  1. Themes customization
  2. Notification sounds
  3. Typing indicators

## Acknowledgments

  1. Java Swing documentation
  2. Oracle Networking tutorials
  3. Stack Overflow community


