# Server Performance Stats

A lightweight Bash script for monitoring Linux server performance metrics in real-time.

## Project URL
https://roadmap.sh/projects/server-stats

## Description

This script provides a simple and efficient way to monitor key system performance indicators including CPU usage, memory consumption, disk usage, and process information. It's designed for system administrators and DevOps engineers who need quick insights into server health.

## Features

- **CPU Usage**: Display total CPU utilization percentage
- **Memory Usage**: Show memory statistics (Free, Used, and Cache percentages)
- **Disk Usage**: Display root partition disk usage
- **Process Monitoring**: List top 5 processes by CPU or memory consumption
- **System Information**: Display OS version and uptime

## Requirements

- Linux operating system
- Bash shell
- Standard utilities: `top`, `df`, `awk`, `uname`, `w`

## Installation

1. Clone or download the script:
   ```bash
   git clone <repository-url>
   cd server_performance_stats
   ```

2. Make the script executable:
   ```bash
   chmod +x server-stats.sh
   ```

## Usage

Run the script with one of the following options:

```bash
./server-stats.sh [OPTION]
```

### Options

| Option | Description |
|--------|-------------|
| `-h` | Display help message |
| `-c` | Show total CPU usage |
| `-m` | Show total memory usage (Free vs Used including percentage) |
| `-d` | Show total disk usage (Free vs Used including percentage) |
| `-P` | Display top 5 processes by CPU usage |
| `-M` | Display top 5 processes by memory usage |
| `-a` | Display all metrics (comprehensive report) |

### Examples

**Show all metrics:**
```bash
./server-stats.sh -a
```

**Check CPU usage only:**
```bash
./server-stats.sh -c
```

**Check memory usage:**
```bash
./server-stats.sh -m
```

**View top CPU-consuming processes:**
```bash
./server-stats.sh -P
```

## Sample Output

```
System Monitor Report
---------------------------------------------------------------------------------------
os version: Linux hostname 5.15.0-91-generic #101-Ubuntu SMP x86_64 GNU/Linux
uptime: 10:30:45 up 5 days, 3:15, 2 users, load average: 0.45, 0.52, 0.48
---------------------------------------------------------------------------------------

CPU Usage: 23.5%
Memory Usage: 45.2% Free, 42.1% Used, 12.7% Cache
Disk Usage: 68%

---------------------------------------------------------------------------------------

Top 5 processes by CPU usage: 
  PID USER      PR  NI    VIRT    RES    SHR S  %CPU  %MEM     TIME+ COMMAND
 1234 user      20   0 2456788 345678  98765 S  12.5   5.4   1:23.45 firefox
 5678 user      20   0 1234567 234567  87654 S   8.3   3.2   0:45.67 chrome
```

## License

This project is open source and available for free use.

## Contributing

Contributions, issues, and feature requests are welcome!

## Author

Created as a system monitoring tool for Linux servers.
