# MikroTikUtils

**MikroTikUtils** is a collection of [RouterOS](https://mikrotik.com/software) scripts designed to automate and enhance MikroTik device management. Some scripts use Telegram bots for notifications. You must already have a Telegram bot or create a new one to use notification features.


## Features

- Monitor and notify on IP address changes via Telegram ([`IPchanged.rsc`](IPchanged.rsc))
- Easily configurable notification settings
- Modular scripts for various automation tasks
- Designed for easy integration into MikroTik devices


### Requirements

- MikroTik device running RouterOS
- Access to the MikroTik terminal or Winbox
- (Optional) [Telegram bot](https://core.telegram.org/bots#6-botfather) for notifications


### Installation

1. **Clone or Download** this repository:
    ```sh
    git clone https://github.com/yourusername/MikroTikUtils.git
    ```
    Or download the scripts directly from the [GitHub repo](https://github.com/yourusername/MikroTikUtils).

2. **Upload Scripts**  
   Use Winbox, WebFig, or FTP to upload the desired `.rsc` script(s) to your MikroTik device.

3. **Import Script**  
   In the MikroTik terminal, run:
    ```
    /import file-name=IPchanged.rsc
    ```
   Replace `IPchanged.rsc` with the script you want to import.

4. **Configure Telegram Bot (if needed)**  
   - Create a Telegram bot via [BotFather](https://core.telegram.org/bots#6-botfather).
   - Set your bot token and chat ID in the configuration file script `TelegramConfig.rsc`.


## Usage

**Example:**  
To use the IP change notification script:
1. Edit the `TelegramConfig` script with your bot token and chat ID.
2. Import or create (copy/paste) both `TelegramConfig` and `IPchanged.rsc` scripts.
3. Schedule the script to run periodically using the MikroTik scheduler.


## Security Notes

- Scripts do **not** contain hardcoded credentials by default.
- Always review and test scripts in a safe environment before deploying to production.
- Protect your Telegram bot token and chat ID.


## Contributing

Contributions, issues, and feature requests are welcome!  
Feel free to [open an issue](https://github.com/yourusername/MikroTikUtils/issues) or submit a pull request.


## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.


## Author

CtrlAltJon

