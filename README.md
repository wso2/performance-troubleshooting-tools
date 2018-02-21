# Java Troubleshooting Tools
This repository contains some tools to troubleshoot Java related performance issues.

The tools are basically shell scripts (compatible with Bash 4.x).

All commands support `-h` option to show the usage of the commands

Following are the tools available

* [top-threads](#top-threads)
* [jstack-profiler](#jstack-profiler)
* [analyze-jstack-samples](#analyze-jstack-samples)

## top-threads

Show top CPU consuming threads in a Java process.

This tool uses `ps` command to get the CPU usage of individual threads

## jstack-profiler

Naive Java Profiler, which uses the `jstack` command to take thread dump samples in specified intervals.

All thread dumps will be saved in a single directory.

This tool also saves the `ps` command output, which has the CPU usage for each thread.

## analyze-jstack-samples

This tool analyzes the `jstack` thread dump samples taken from `jstack-profiler` tool.

There are two reports.

1. Stack Samples Count by Thread State (Default report)
2. Average CPU Usage of Threads (using both thread dump and `ps` output)
