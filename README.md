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
