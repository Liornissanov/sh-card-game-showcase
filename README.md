# SH – CARD GAME

A landscape multiplayer card game for Android and iOS, built with **Flutter** and **Dart**. It adapts the classic Shed (Palace) rules for local pass-and-play and private online matches. Players play through their hand, face-up cards, and face-down cards. The last player with cards loses.

## Gameplay

- Play locally or create a private online room for friends.
- Use special cards, watch animated card reveals, and play with a countdown in online matches.
- Rejoin a room after a dropped connection or spectate after finishing your hand.

## How it works

| Component | Role |
| --- | --- |
| Flutter client | Renders the table, cards, animations, and room screens. |
| Pure-Dart rules engine | Validates moves and resolves turns for both local and online play. |
| Dart WebSocket server | Manages rooms, validates online moves, and sends updated match state to clients. |
| Supabase | Supports player accounts and coin balances. |

The same rules engine runs on the device for local games and on the server for online matches. Keeping the rules in a separate Dart package lets the client and server use the same move validation while the server remains authoritative online.
