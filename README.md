import datetime
import subprocess

# Path to the log file
file_path = "daily_log.txt"

# Write the current date and time to the file
with open(file_path, "a") as f:
    f.write(f"Updated on: {datetime.datetime.now()}\n")

# Run git commands to commit and push
subprocess.run(["git", "add", file_path])
subprocess.run(["git", "commit", "-m", "Daily update"])
subprocess.run(["git", "push"])
# GitHub Activity Keeper 🟢

This script helps you stay active on GitHub by making automatic daily commits.

## How It Works

- Updates a `daily_log.txt` file with the current date/time
- Automatically commits and pushes the change

## How to Use

1. Clone your GitHub repo or create a new one.
2. Add this script inside the repo.
3. Run it manually or schedule it to run daily.

```bash
python3 daily_commit.py
