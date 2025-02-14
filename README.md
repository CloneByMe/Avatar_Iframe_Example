Avatar Integration Example
==========================

This project is a demonstration of how to integrate our avatars into a website via an iframe. The example shows how to:

- Receive Messages: Listen for messages from the iframe (e.g., questions and images).
- Send Messages: Send text to the avatar for it to speak.

Features
--------
- Embedded Iframe: Loads the avatar chat widget.
- Bidirectional Communication: Uses postMessage for message exchange between the parent page and the iframe.

Getting Started
---------------
1. Clone the Repository:

   git clone https://github.com/yourusername/avatar-integration.git

2. Configure the Avatar Token:

   Open the index.html file and replace [YOUR_AVATAR_TOKEN] in the iframe URL with your actual avatar token.

3. Run the Example:

   Open the index.html file in your browser (either directly or using a local web server).

How It Works
------------
The iframe loads the chat widget from:

   https://app.clonebyme.com/chat-widget?avatar=[YOUR_AVATAR_TOKEN]

The JavaScript in the page handles:

- Listening for Messages: It listens for messages from the iframe and displays them in the appropriate section.
- Sending Messages: It sends text entered by the user to the iframe so that the avatar can speak it.

Contributing
------------
If you want to improve this example or adapt it to your needs, feel free to submit a pull request or open an issue.

License
-------
Unlicense
