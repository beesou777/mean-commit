# DailyMdCommits: Randomized Daily Commits

Welcome to the **DailyMdCommits** repository! This project is set up to automatically commit a message to this repository every day. The message includes a greeting along with a random number sequence like `32443` or `12345!?`.

## What Does This Repository Do?

This repository automatically commits a file named `random_text.md` with the following content:
- A greeting: `"Hello, my name is bishwa shah"`
- A randomized number sequence, such as `1337`, `31337!?`, etc.

These commits are made daily using GitHub Actions.

## How It Works

- **GitHub Actions** triggers a workflow daily at midnight (UTC).
- The workflow generates a random 4-digit number with a 50% chance of adding `!?` at the end.
- It writes the message and random number to `random_text.md`.
- The changes are then committed and pushed to the repository automatically.

## About the Author

- **Name:** bishwa jung shah
- **Username:** beesou777
- **Email:** sbeesou@gmail.com

Thank you for checking out this repository!

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
