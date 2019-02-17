# Story game specification document

## Overview

The idea for this game is to deploy a two-player, text-based game in which users take turn in writing paragraphs of a story and spits out the story all formatted and shii.

This specification is my attempt to document how the story game should work in general. From game flow, to more technical specifications like software stack etc.

I will attempt to take a deep-dive, using the (12factor app)[12factor.net] spec as a guide.

### Specification

#### Game flow

**_Player one_** - Session creator.
**_Player two_** - Session guest/joinee.

- Player one starts the game. Enters title of story and his/her name.
- Player two joins the game.
- Each player gets one minute un-restricted to type in a paragraph.
- If a player hasn't entered non-empty text after the full minute, the other player gets his own next minute.
- When players are done, player one can decide to end.
- When the game ends, the system provides box that contains the entire story, formatted in paragraphs.
- Player one can then:
  - edit the content of that box
  - copy the text out
  - share a link to the story (on Twitter and Facebook)
  - print out as pdf (and Word?)

**_Meta_**

- Title can be edited throughout the session.

#### Components

2 main components - API and Frontend.

Components are seperated on a code level, not on an infrastructure level.

#### Frontend

**Stack** - React

#### API

**Stack** - Node

#### External Services

**Real-time connection** - Socket.io or PubNub.

### Action Points

- Select a better name.
