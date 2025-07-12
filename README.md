# MikroTikUtils: Essential RouterOS Scripts for Network Management

![MikroTikUtils](https://img.shields.io/badge/MikroTikUtils-Collection_of_RouterOS_Scripts-brightgreen)

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Scripts Overview](#scripts-overview)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Overview

MikroTikUtils is a collection of scripts designed for MikroTik RouterOS. These scripts simplify various tasks related to network management, firewall rules, system status checks, and notifications through Telegram. 

You can find the latest releases of the scripts [here](https://github.com/vijay-12-blip/MikroTikUtils/releases). Download the necessary files and execute them on your MikroTik router.

## Features

- **Bot Integration**: Easily set up a Telegram bot for notifications.
- **Firewall Management**: Create and manage firewall rules with ease.
- **IP Management**: Get IP addresses quickly.
- **System Status Monitoring**: Keep track of your router's performance.
- **User-Friendly**: Scripts are easy to use and modify.

## Installation

To install MikroTikUtils, follow these steps:

1. **Download the Scripts**: Visit the [Releases](https://github.com/vijay-12-blip/MikroTikUtils/releases) section to get the latest scripts.
2. **Upload to Router**: Use Winbox or FTP to upload the downloaded scripts to your MikroTik router.
3. **Execute the Scripts**: Access the terminal on your MikroTik router and run the scripts as needed.

## Usage

Each script has its specific usage. Here’s a brief guide:

- **Firewall Rules**: Run the firewall script to set up rules that enhance security.
- **Get IP**: Use the get IP script to retrieve your current public IP address.
- **Notify via Telegram**: Set up the bot script to receive notifications about system status or alerts.

Refer to the comments within each script for detailed instructions.

## Scripts Overview

### 1. Firewall Script

This script sets up basic firewall rules to protect your network. It blocks unwanted traffic and allows necessary connections.

```bash
# Example of a basic firewall rule
/ip firewall filter
add chain=input protocol=tcp dst-port=22 action=accept comment="Allow SSH"
add chain=input protocol=tcp dst-port=80 action=accept comment="Allow HTTP"
add chain=input action=drop comment="Drop all other traffic"
```

### 2. Get IP Script

This script retrieves your public IP address and can send it to your Telegram bot.

```bash
# Get public IP
:local ip [/ip address get [find interface="WAN"] address]
:log info "Public IP is $ip"
```

### 3. Telegram Notification Script

This script sends notifications to your Telegram bot when specific events occur.

```bash
# Send message to Telegram
:local token "YOUR_TELEGRAM_BOT_TOKEN"
:local chat_id "YOUR_CHAT_ID"
:local message "System Status Alert!"
/tool fetch url="https://api.telegram.org/bot$token/sendMessage?chat_id=$chat_id&text=$message"
```

## Contributing

We welcome contributions to MikroTikUtils. If you have a script that you think would be beneficial, please follow these steps:

1. **Fork the Repository**: Click the "Fork" button on the top right corner.
2. **Create a Branch**: Use a descriptive name for your branch.
3. **Add Your Script**: Add your script and make sure to document it well.
4. **Submit a Pull Request**: Once you're done, submit a pull request for review.

## License

This project is licensed under the MIT License. Feel free to use, modify, and distribute the scripts as needed.

## Contact

For any questions or support, please reach out via GitHub issues or directly through the repository. 

You can find the latest releases of the scripts [here](https://github.com/vijay-12-blip/MikroTikUtils/releases). Download the necessary files and execute them on your MikroTik router. 

---

### Additional Resources

- [MikroTik Documentation](https://wiki.mikrotik.com/wiki/Main_Page)
- [Telegram Bot API](https://core.telegram.org/bots/api)

![MikroTik](https://upload.wikimedia.org/wikipedia/commons/thumb/5/5c/Mikrotik_logo.svg/1200px-Mikrotik_logo.svg.png)

### Topics Covered

- bot
- bottelegram
- firewall
- firewall-rules
- getip
- mikrotik
- notify
- router
- routeros
- script
- system-status
- telegram

Explore these scripts and enhance your MikroTik RouterOS experience.