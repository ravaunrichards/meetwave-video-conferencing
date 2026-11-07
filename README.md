# MeetWave — Video Conferencing Starter

An independent browser-based video meeting project. It is not affiliated with Zoom or any other meeting provider.

## Features
- Responsive meeting lobby with create/join by room code.
- Browser microphone/camera permissions and local preview.
- WebRTC peer-to-peer audio/video and screen sharing.
- Real-time meeting chat and participant updates over WebSockets.
- Mute/unmute, camera toggle, leave meeting, invite-link copy.
- Server-side room validation and a maximum of 8 participants per room in this starter.
- Health and room-status endpoints.

## Requirements
Node.js 20 or newer. Modern browser. Camera/microphone access requires localhost or HTTPS. WebSocket signaling runs through the same server.

## Run locally
```bash
npm install
npm test
npm start
```
Then open http://localhost:3000 in a modern browser. Use a second browser/device on the same reachable server and enter the same room code to test a meeting. For phones or other devices, localhost on the server machine is not their localhost; use a reachable HTTPS deployment.

## Important limitations
This is a functional prototype/starter, not a production-ready Zoom replacement. WebRTC uses a public STUN server and no TURN relay, so connections can fail on restrictive networks. Mesh conferencing has limited scaling; the eight-participant cap is intentional. No accounts, waiting room, moderator permissions, meeting passwords, recordings, calendar integration, cloud recording, end-to-end encryption review, abuse controls, or enterprise access management are included. Before public use, deploy behind HTTPS/WSS, add TURN and preferably an SFU such as LiveKit/mediasoup, enforce authenticated room access and rate limits, and review privacy/security requirements. Do not use for sensitive meetings without a proper security review.
