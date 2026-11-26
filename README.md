# LogLens

Loglens is a Python program that counts records in CSV log files based on their log level. Users can count all records or select a specific log level. The program runs locally and does not change the original file. LogLens is mainly for computing students and new technical interns who have basic knowledge of CSV files and terminal commands.

## Requirements and things

You need Python. Most computers already have it, and version 3.6 or later should be good enough. It works on Windows, Mac, and Linux. Other than that, there is not much to know.

## Get started

First, get the project files from GitHub. Then install the program using `pip install log-lens` and run it by typing `loglens`. If you can't make it work, see docs/INSTALL.md. You probably won't need those instructions.

## Using the program

Run the following command after you have found the correct folder:

`loglens --input mylog.csv --severity error`

The software scans your log, fixes mistakes, and shows you what went wrong. You will see a number once it is finished. You can also run it on real production files without worrying about any side effects.

## Input format

The input should be a CSV file. Log files tend to have fields describing the time and what happened, but LogLens is flexible and will work with whatever columns your monitoring system uses. A small example is included somewhere in this repository.

## Questions

If something doesn't work, just contact the developers or create an issue. Make sure you describe the problem so somebody can help. This is a basic tool, so the instructions should be pretty obvious.
