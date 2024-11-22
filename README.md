# AtlasConnect Messaging Service For Local Networks (Currently)

## How does AtlasConnect work?
AtlasConnect sends messages with the **AtlasConnect Message Packet (ACMP)** and it is divided into multiple parts to handle the data.

**CURRENTLY ONLY TWO TYPES OF DATA ARE PROVIDED**
1. 255 bytes (characters without `\0` (termination character) uncounted) are message contents, may be expanded if needed.
2. 9 bytes (characters without `\0` (termination character) counted) are name data, probably won’t be expanded.

## How to install AtlasConnect
**SIMPLE**, just copy the `AtlasConnect.tar.gz` file to `/usr/bin` and unzip it. Two files will be added to `/usr/bin`:
  1. `atlasconnect_server`: The server program, has a built-in command line interpreter (100 USERS MAX).
  2. `atlasconnect_client`: The client program, nothing special, asks for name before starting conversations.

## ___ How to use the server command line interpreter?
**SIMPLE**, command list below:
- `/clients`: Lists clients with IDs and names.
- `/kick username` (8 chars max): Kicks a client.
- `/ban username` (8 chars max): Bans a client (temporary until server is shutdown).
- `/exit`: Shuts down the server.

## **Features:**
  1. Uses SQLite3 to save (TEMP) user data.
