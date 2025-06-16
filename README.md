# TarinWelcomer - Advanced Discord Welcome Bot

TarinWelcomer is a powerful and feature-rich Discord bot built with Node.js and `discord.js` v14. It goes beyond simple text messages by generating custom, high-quality image banners to welcome new members and announce departures. With advanced features like invite tracking and role persistence, it provides a professional and engaging experience for any Discord server.

![Welcome Banner Example](https://github.com/user-attachments/assets/2b314afa-53de-4c83-9e6d-f0a5dec6f9a5)
*(Example of a generated welcome banner)*

## ✨ Key Features

* 🖼️ **Dynamic Welcome & Leave Banners**: Automatically generates personalized images using `node-canvas` when a user joins or leaves, incorporating their avatar, username, and ID onto a custom background.
* 🔗 **Advanced Invite Tracking**: Accurately detects which invite a new member used to join, gives credit to the inviter, and updates their total invite count in the database.
* 🔄 **Role Persistence**: Remembers a user's roles when they leave the server. If they rejoin, the bot automatically restores their previous roles, saving administrators time.
* 📊 **Live Server Stats**: Keeps a voice channel updated with the server's current member count, providing an easy-to-see statistic.
* ⚡ **Modern Slash Command Handler**: Features a robust, file-based handler that automatically registers and loads all slash (`/`) commands from the `/commands` directory.
* ⚙️ **Highly Configurable**: Easily manage all server-specific IDs, channels, and roles from a central `config.js` file.
* 💾 **Database Integration**: Utilizes a database to persistently store user information, invite counts, and role backups.

## 🛠️ Setup & Installation

Follow these steps to get the bot running on your own server.

### Prerequisites

* [Node.js](https://nodejs.org/en/) (v22.9.0 or higher is recommended)
* A Discord Bot Token

### 1. Clone the Repository

```bash
git clone [https://github.com/your-username/TarinWelcomer.git](https://github.com/Maniseniler/TarinWelcomer.git)
cd TarinWelcomer
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Configure the Bot
Create a `config.js` file in the root directory and populate it with your server's information.
```js
// config.js
module.exports = {
    // --- Bot Credentials ---
    clientTOKEN: "YOUR_DISCORD_BOT_TOKEN",
    clientID: "YOUR_BOTS_CLIENT_ID",

    // --- Server & Channel IDs ---
    serverID: "YOUR_GUILD_ID",
    infoChannel: "VOICE_CHANNEL_ID_FOR_MEMBER_COUNT",
    welcomeChannel: "CHANNEL_ID_FOR_WELCOME_MESSAGES",
    leftChannel: "CHANNEL_ID_FOR_LEAVE_MESSAGES",

    // --- Role IDs ---
    memberRole: "DEFAULT_MEMBER_ROLE_ID",
    customerRole: "CUSTOMER_ROLE_ID_FOR_STATUS", // Optional, used for presence status

    // --- Bot Info ---
    name: "TarinWelcomer",
    devs: ["YOUR_DISCORD_USER_ID"],
};
```
