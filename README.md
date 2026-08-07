MindPlaceSecure

MindPlaceSecure is a static web-based chatroom and room configuration experience built for secure, private, peer-to-peer messaging. The site provides a simple landing page, room creation and joining flow, a configurable room interface, and supporting informational pages about how the system works and its accessibility features.


Vercel Host Link: https://mind-place-secure-website-host.vercel.app/



Overview
1. Landing page: users enter a room ID and optional username to start or join a room.
2. Room interface: hosts and guests can connect through a WebSocket signaling server and establish a direct peer-to-peer chat channel.
3. Configuration page: users can set room details and preferences before entering the room.
4. Informational pages: the site includes architecture, setup, accessibility, reporting, and how-it-works content.

How to use
1. Open the site in a browser.
2. Enter a room ID and username on the main page, or choose Provision New ThinkSpace.
3. Use the same room ID in another browser tab or device to join the same room.
4. Start chatting once the P2P connection is established.

Setup
1. Install the signaling server dependencies:
   - cd signaling-server
   - npm install
2. Start the signaling server:
   - npm start
3. Serve the frontend locally if needed:
   - python -m http.server 8000
4. Open http://127.0.0.1:8000 in a browser.

Deployment
1. The frontend can be deployed to view in Github as a static site as well as Vercel but be sure to run the setup before testing the site.
2. The signaling server must be hosted separately because it uses long-running WebSocket connections.
3. Update config.js with the production signaling server URL before deploying.

Files
1. index.html: main entry page.
2. room.html: chat room interface and peer connection logic.
3. configure.html: room configuration interface.
4. signaling-server/server.js: WebSocket signaling server.
5. config.js: configurable signaling server URL.
6. vercel.json: Vercel routing configuration.
