# AD Username Generator

A Python script for generating potential Active Directory usernames based on common corporate naming conventions.

## Purpose
This tool is designed for penetration testers and security professionals to generate comprehensive username lists for activities like password spraying attacks, user enumeration, and security assessments.

## Features
- Supports multiple input formats (space-separated, dot-separated, CSV)
- Generates 19 username variations per user
- No external dependencies
- Handles UTF-8 encoding

## Installation
```bash
# No installation required - just Python 3.6+
python ad_username_generator.py employees.csv
```

## Usage
```bash
python ad_username_generator.py <input_file>
```

## Input Formats
### Single column (space):
```bash
john doe
jane smith
```
### Single column (dot):
```bash
john.doe
jane.smith
```
### Two columns:
```bash
john,doe
jane,smith
```

### Examples
```bash
# Basic usage
python ad_username_generator.py employees.csv

# Save to file
python ad_username_generator.py employees.csv > usernames.txt

# Use with password spray tools
python ad_username_generator.py employees.csv | kerbrute userenum --dc DC_IP [IP]
```
### Output
For "john doe", generates:

- johndoe, john.doe, john-doe

- johdoe, joh.doe, joh-doe

- jdoe, j.doe, j-doe

- doejohn, doe.john, doe-john

- doejoh, doe.joh, doe-joh

- djohn, d.john, d-john

- doej, doe.j, doe-j

### Legal Notice
Use only for authorized security testing with proper permission.
