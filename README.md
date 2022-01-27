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

## Tech Stack
- Created using Node.js, Express, Socket.io, and Mustache.js
