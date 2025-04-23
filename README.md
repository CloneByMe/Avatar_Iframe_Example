# 🧠 Avatar Integration Example | CloneByMe

This project demonstrates how to embed a CloneByMe avatar into a webpage using an iframe. It allows full bidirectional communication: receive messages like text and images from the avatar, and send spoken responses back.

---

## 🚀 Features

- Interactive avatar embedded using an iframe.
- Real-time message exchange using `postMessage`.
- Displays received text and images from the avatar.
- Sends text input to the avatar for spoken output.
- Optional controls for advanced UI customization inside the iframe.

---

## 🛠️ Installation & Usage

1. **Clone this repository**:
   ```bash
   git clone https://github.com/CloneByMe/Avatar_Iframe_Example.git
   cd Avatar_Iframe_Example
   ```

2. **Configure your avatar token**:  
   Open the `index.html` file and replace the following line:

   ```js
   const AVATAR_TOKEN = "[YOUR CLONEBYME PARTNER TOKEN]";
   ```

   Get your token from your account at [CloneByMe](https://app.clonebyme.com) under the Share page of your avatar.

3. **Open the file in your browser**:  
   You can run the project by simply opening `index.html` in a web browser.

---

## ⚙️ How It Works

- The avatar chat widget is loaded from:
  ```
  https://app.clonebyme.com/chat-widget?avatar=[YOUR_AVATAR_TOKEN]
  ```

- **Receiving Messages**:
  - `NEW_QUESTION`: A text message from the user inside the iframe.
  - `NEW_IMAGE`: A base64 image string received from the iframe.

- **Sending Messages**:
  - `TALK`: Sends a string of text to the avatar so it can speak it aloud.

---

## 💬 Message Flow Examples

**Send a message to the avatar**:
```js
iframe.contentWindow.postMessage({ type: "TALK", message: "Hello there!" }, "*");
```

**Listen for a question from the iframe**:
```js
window.addEventListener("message", (event) => {
  if (event.data?.type === "NEW_QUESTION") {
    console.log("Received question:", event.data.message);
  }
});
```

**Listen for an image**:
```js
window.addEventListener("message", (event) => {
   if (event.data?.type === "NEW_IMAGE") {
   const imageSrc = event.data.imageBase64;
   // Display or handle image
   }
});
```

---

## 🧩 Optional Features

- `setStateOfTypingDots(true/false)`: Toggle visibility of typing indicator dots inside the iframe.
- `showMessagesContainer(true/false)`: Show or hide the message container in the iframe.
- `showClearConversationBtn(true/false)`: Show or hide the clear conversation button inside the iframe.

---

## 🤖 Requirements

- An account on [CloneByMe](https://app.clonebyme.com).
- A valid avatar token.
- Basic understanding of HTML and JavaScript.

---

## 📄 License

Unlicense

---

Build rich, interactive experiences by embedding CloneByMe avatars into your web projects!

