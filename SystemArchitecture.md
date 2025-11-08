  Telex Desktop Notifications

## 🏗️ Overview
The Telex Desktop Notification System delivers real-time alerts to desktop users.  
It connects the backend (where messages are generated) with the Electron-based desktop client, ensuring instant delivery and smooth UX.

## 🧠 Tech Stack

| Layer | Technology | Description |
|-------|-------------|-------------|
| Frontend | Electron.js, React.js | Desktop UI and OS notifications |
| Backend | Node.js, Express | Handles API logic and routing |
| Database | MongoDB / Firebase | Stores messages and notifications |
| Communication | WebSockets | Real-time data transfer |
| Notification API | Native OS APIs | Pop-ups and sound alerts |

## 🔄 Communication Flow
1. User sends a message in Telex.  
2. Backend processes it and emits via WebSocket.  
3. Desktop client listens for events.  
4. When received, it triggers a desktop alert and sound.  
5. If offline, the message is queued and delivered later.

## 🧬 Data Flow Example
```json
{ "type": "new_message", "sender": "John", "message": "Team meeting starts now!" }
