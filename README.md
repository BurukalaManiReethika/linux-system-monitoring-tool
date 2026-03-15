# linux-system-monitoring-tool
Linux System Monitoring Tool written in C to monitor CPU, memory, and system processes.
# Linux System Monitoring Tool

A simple Linux System Monitoring Tool developed in C that tracks system performance such as CPU usage, memory usage, and running processes.

## Features
- CPU usage monitoring
- Memory usage monitoring
- Process tracking
- Linux system calls

## Technologies Used
- C Programming
- Linux
- GCC Compiler

## How to Run

Compile the program:

gcc monitor.c -o monitor
# Generate the full PDF with code and documentation for the Linux System Monitoring Tool

from reportlab.platypus import SimpleDocTemplate, Paragraph, Spacer, Preformatted
from reportlab.lib.styles import getSampleStyleSheet
from reportlab.lib.pagesizes import A4

file_path = "/mnt/data/linux_system_monitoring_tool_full_code.pdf"

styles = getSampleStyleSheet()

title = Paragraph("Linux System Monitoring Tool (C + Linux) – Full Code & Documentation", styles['Title'])

overview = Paragraph(
"""<b>Project Overview</b><br/>
This project is a Linux System Monitoring Tool written in C. It reads system data from the Linux
/proc filesystem and displays CPU information, memory usage, system uptime, load average,
and the total number of running processes. The tool refreshes every 5 seconds to provide
near real-time monitoring.""",
styles['BodyText']
)

structure = Preformatted(
"""Project Structure

linux-system-monitoring-tool
│
├── monitor.c
├── Makefile
└── README.md
""", styles['Code']
)

monitor_code = Preformatted(r"""
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include <unistd.h>

void cpu_usage() {
    FILE *fp;
    char buffer[1024];

    fp = fopen("/proc/stat", "r");
    if (fp == NULL) {
        printf("Unable to read CPU info\n");
        return;
    }

    fgets(buffer, sizeof(buffer), fp);
    printf("CPU Info: %s\n", buffer);

    fclose(fp);
}

void memory_usage() {
    FILE *fp;
    char buffer[256];

    fp = fopen("/proc/meminfo", "r");
    if (fp == NULL) {
        printf("Unable to read memory info\n");
        return;
    }

    printf("\nMemory Information:\n");

    for(int i=0;i<5;i++){
        fgets(buffer, sizeof(buffer), fp);
        printf("%

Run the program:

./monitor

## Output Example
Displays CPU usage, RAM usage, and running processes.

## Author
Your Name BURUKALA MANI REETHIKA
