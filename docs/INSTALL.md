# LogLens Installation Guide

This guide explains how to set up and run LogLens. It is intended for computing students and new technical interns who are familiar with CSV files and terminal commands.

## Requirements

- Python 3.10 or newer
- A terminal
- A CSV log file (a sample file is included in the repository)
To check your Python version, run:
```bash
python --version
```
On some computers such as mac, you may need to use `python3` or `py` instead of `python`.
LogLens uses only the Python standard library, so no additional packages are required. It processes log files locally without uploading them.

## Getting the program

Get LogLens from the GitHub website. Look for the green button and download a ZIP. Then extract it. Make sure you are in the right place in the terminal, because you will need that later. Once everything is done, you can install it.

Run this command:

pip install loglens

Then move on to the next step.

## Running a check

First, take a CSV file from your logging system and put it in the project directory. It needs the columns `date`, `severity`, and `details` or the tool might fail. Running it is easy:

python loglens.py data/sample_logs.csv

For your own files, type `python loglens.py --file /Users/alex/Desktop/system-log.csv --level error`. This will print results when the analysis is over. You can find the example data in the project somewhere.

## Problems and fixes

If you see a "file not found" error, reinstall Python and try again. If the software complains about the CSV, there might be something wrong with your system. If none of this works, open a public GitHub issue and attach your entire original CSV so the team can investigate. Please do not waste the maintainers' time with problems caused by skipped steps.
