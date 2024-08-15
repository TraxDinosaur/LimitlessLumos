# LimitlessLumos

**LimitlessLumos** is a Python package that provides a simple and efficient solution to keep Telegram bots and other long-running scripts alive indefinitely. It leverages Flask to create a lightweight web server, ensuring that your bots or scripts remain active and operational.

## Features

- **Keep Alive**: Utilizes a Flask-based server to prevent your script from timing out.
- **Threading Support**: Runs the Flask server in a separate thread, allowing your script to continue running concurrently.
- **Easy Integration**: Simple to integrate into existing Python scripts or Telegram bots.

## Installation

You can install **LimitlessLumos** via pip. Make sure you have Python 3.6 or higher installed.

```bash
pip install LimitlessLumos
```

## Usage

Here’s a basic example of how to use **LimitlessLumos** to keep your script running:

1. **Create your script** (e.g., `my_bot.py`):

    ```python
    from limitless_lumos import lumosServer
    from my_telegram_bot import start_bot  # Replace with your bot’s start function

    # Start your bot or script
    start_bot()

    # Keep the script running indefinitely
    lumosServer()
    ```

2. **Run your script**:

    ```bash
    python my_bot.py
    ```

This example assumes you have a `start_bot` function in `my_telegram_bot.py` that initiates your Telegram bot. The `lumosServer` function will keep your script alive by running a Flask server in a separate thread.

## Configuration

**LimitlessLumos** uses Flask, which listens on `0.0.0.0` by default. You can customize the server configuration by modifying the `lumosServer` function in the package or by adjusting the Flask app settings.

## Contributing

Contributions are welcome! If you have suggestions or improvements, please fork the repository and submit a pull request.

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/your-feature`).
3. Commit your changes (`git commit -am 'Add new feature'`).
4. Push to the branch (`git push origin feature/your-feature`).
5. Create a new Pull Request.

## License

**LimitlessLumos** is licensed under the [CC-BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) license.

## Contact

For any questions or support, please reach out to [TraxDinosaur](https://traxdinosaur.github.io).
