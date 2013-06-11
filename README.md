strophe.jingle
==============

webrtc connection plugin for [strophe.js](http://strophe.im/strophejs/). Strophe  is a popular library for writing XMPP client applications that run on any of the current popular browsers. Instead of the native TCP binding, strophe.js uses BOSH (Bidirectional-streams Over Synchronous HTTP, a variant of long polling) to connect to an XMPP server. Besides enabling anyone to build (federated) IM applications, this opens up the browser as an addressable endpoint for two-way exchange of structured messages, including presence and publish-subscribe applications.

This plugin WebRTC makes it possible to negotiate audio/video streams via XMPP and then relinquish control to the WebRTC support of browsers like Firefox and Chrome for the actual out-of-band media streams. XMPP/Jingle you get the authenticated, secured and federated media signaling, whereas WebRTC gives you an API to set up the media streams using RTP/ICE/STUN and provide access to cameras and microphones.

Features:
- mostly standards-compliant jingle, mapping from WebRTCs SDP to Jingle and vice versa. Aiming for full compliance.
- tested with chrome and firefox.
- trickle and non-trickle modes for ICE (XEP-0176). Even supports early candidates from peer using PRANSWER.
- support for fetching time-limited STUN/TURN credentials through XEP-0215. [rfc5766-turn-server](https://code.google.com/p/rfc5766-turn-server/) is a TURN server which implements this method.

