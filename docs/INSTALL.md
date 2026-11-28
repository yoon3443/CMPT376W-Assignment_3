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

## Setting Up LogLens
1. Open the GitHub repository.
2. Click Code → Download ZIP
3. Extract the downloaded ZIP file.
4. Open a terminal.
5. Navigate to the extracted folder using the `cd` command.

Make sure you are in the repository root, which is the folder containing `loglens.py`.

The folder should contain the following files and directories:
```text
loglens.py
README.md
docs/
data/
```
No additional installation is required.

## Running LogLens with the Sample File
Before using your own CSV file, test the program with the included sample file.
Run the following command from the repository root:
```bash
python loglens.py --file data/sample_logs.csv --level ERROR
```
Expected output:
```text
Records matching ERROR: 2
```
To count all records, run:
```bash
python loglens.py --file data/sample_logs.csv
```
Expected output:
```text
Records matching ALL: 6
```

## Preparing Your Own CSV File
Make sure your CSV file contains the following column headers:
- `timestamp`
- `level`
- `message`
The column names must match exactly. The supported log levels are `INFO`, `WARN`, and `ERROR`.
See the [sample CSV file](../data/sample_logs.csv) for an example.

## Running LogLens with Your Own File
Use the `--file` argument to specify your CSV file.
The `--level` argument is optional. If you do not include it, LogLens counts all records.
To see the available command-line options, run:
```bash
python loglens.py --help
```

## Problems and fixes

If you see a "file not found" error, reinstall Python and try again. If the software complains about the CSV, there might be something wrong with your system. If none of this works, open a public GitHub issue and attach your entire original CSV so the team can investigate. Please do not waste the maintainers' time with problems caused by skipped steps.
