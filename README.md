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

## Input format

The input should be a CSV file. Log files tend to have fields describing the time and what happened, but LogLens is flexible and will work with whatever columns your monitoring system uses. A small example is included somewhere in this repository.

## Questions

If something doesn't work, just contact the developers or create an issue. Make sure you describe the problem so somebody can help. This is a basic tool, so the instructions should be pretty obvious.
