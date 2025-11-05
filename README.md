# Port Scanner

A simple Python port scanner for learning and small-scale use.

## Overview
This script allows you to scan either a contiguous port range or a custom list of ports for a given host. It supports:
- Range mode: `python3 port_scanner.py TARGET START_PORT END_PORT`
- List mode: `python3 port_scanner.py TARGET "22,80,1000-1005"`
- Single port mode: `python3 port_scanner.py TARGET 80`

The tool is implemented using only the Python standard library (no external dependencies), and is intended as an educational example rather than a production security tool.

## Features
- Hostname resolution
- Port input parsing (single ports, comma-separated lists, and dash ranges)
- Input validation (ensures ports are within `0-65535`)
- Clear OPEN / CLOSED output per port

## Usage examples
```bash
# Scan a range
python3 port_scanner.py example.com 20 25

# Scan a list of specific ports (use quotes)
python3 port_scanner.py example.com "22,80,443"

# Scan a list with a dash-range inside
python3 port_scanner.py example.com "22,80,1000-1005"
