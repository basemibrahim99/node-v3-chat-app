# 📲 Live Chatroom Web Application 💬
This is a fully functioning live chatroom web application written in JavaScript.\
It can be accessed through this URL: https://ibra-node-chat-app.herokuapp.com/

## How to Use
  - When the web page first loads, a form is shown on the screen prompting the user for a display name and a room name.
  - The user can enter a display name and a chatroom name, then click the join button on the form:
    - If the chatroom doesn't exist, one will be created and the user will be redirected to the chatroom.
    - If the chatroom does exist, the user will join that chatroom with the other user(s) currently in it as well.
    - Display names in chatrooms must be unique, so if you enter an existing chatroom name and a display name that is already in use in said chat room you will be taken back to the form and promtped to enter a valid display name.

## Features
  - Once the user(s) are in a chatroom:    
    - They will be able to view the chatroom name and the list of users who are currently in the chatroom.
    - They will have the ability to send live messages to the chat.
    - They will have the ability to share their current location via a Google Maps link in the chat.

## How it Works
- Created using Node.js, Express, Socket.io, and Mustache.js
- The non-blocking nature of Node makes it well-suited for real-time applicationms such as chat apps, social media apps and more.
- Since the chat application is serving up client-side assets, Express was also used to create the web app.
- Using WebSocket protocol to support features that use bi-directional real-time communication.
  - Socket.io was chosen since it comes with everything needed to set up a WebSocket server using node. Using Socket.io we can:
    -  Listen for events (a new user joining a chatroom or new message being sent to the chat room)
    -  Broadcast/Emit events (sending out messages to particular sockets based on the event)
- The ability to share the user's current location in implemented using the Geolocation API:
  - A check is first made to see if the user's broswer supports the API.
    - If so, a call is made to the API to get the longitude and latitude, they are then injected into a Google Maps URL and sent in the chat.
    - If the browser does not support the API, the user will be notified of this. 
