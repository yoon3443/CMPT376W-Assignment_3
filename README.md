# LogLens

Loglens is a Python program that counts records in CSV log files based on their log level. Users can count all records or select a specific log level. The program runs locally and does not change the original file. LogLens is mainly for computing students and new technical interns who have basic knowledge of CSV files and terminal commands.

## Requirements

Before using LogLens, you need:
- Python 3.10 or newer
- Basic knowledge of CSV files and terminal commands
- A CSV file with the required columns
LogLens does not require any additional packages or installation.

## Get started
1. Click Code → Download ZIP on this GitHub repository.
2. Extract the downloaded ZIP file.
3. Open a terminal and go to the folder containing `loglens.py`.
4. Run the program using the commands below.
For more detailed instructions, see the [Installation Guide](docs/INSTALL.md).

## Usage

Run these commands from the folder containing `loglens.py`.

### Count ERROR Records

```bash
python loglens.py --file data/sample_logs.csv --level ERROR
```

Expected output:
```text
Records matching ERROR: 2
```

### Count All Records

If you do not select a log level, LogLens counts all records.

```bash
python loglens.py --file data/sample_logs.csv
```
Expected output:

```text
Records matching ALL: 6
```

To see the available options, run:

```bash
python loglens.py --help
```

On some computers especially Mac users, you may need to use `python3` or `py` instead of `python`.

## Input Format
LogLens requires a CSV file with these three columns:

| Column | Description |
| --- | --- |
| `timestamp` | The time of the log record |
| `level` | The log level |
| `message` | The log message |

The column names must be exactly `timestamp`, `level`, and `message`.
LogLens supports three log levels: `INFO`, `WARN`, and `ERROR`.
You can find an example file at [data/sample_logs.csv](data/sample_logs.csv).

## Troubleshooting

If the program does not work, check the following:
1. Check if the version is Python 3.10 or newer.
2. Check that you are in the correct folder.
3. Check the CSV file path is correct.
4. Check that the CSV file has the required columns.
5. Check that the log level is `INFO`, `WARN`, or `ERROR`.

For more help, see the [Installation Guide](docs/INSTALL.md).
If you still have problems, you can open a GitHub issue. Explain the problem and include a small example if needed. Do not share any private or sensitive information from your log files.
