# TimeNow

A tiny shell script for quick, directory-specific note-taking in your terminal.

## The Problem

Your notes and todos should be where you are. If you spend your day in the terminal, you shouldn't have to leave it just to jot down a thought, track your progress, or note an idea.

## The Solution

`timenow` is a simple script that lets you quickly capture timestamped notes without leaving your command line.

Because it saves notes to a `timelog.md` file **in your current working directory**, your notes for different projects never get mixed up. It's a quick, dirty, and effective way to keep track of what you're doing, right where you're doing it.

## Usage

### Log a timestamp
```bash
timenow
```
> Logged to ./timelog.md: 2025-11-13T15:00:00+00:00

### Log a timestamp with a comment
```bash
timenow "Finished refactoring the auth module"
```
> Logged to ./timelog.md: 2025-11-13T15:01:00+00:00 - Finished refactoring the auth module

### List the last 10 entries
```bash
timenow list
```
> ---
> Showing last 10 entries from ./timelog.md:
> ---
> * 2025-11-13T15:01:00+00:00 - Finished refactoring the auth module
> * 2025-11-13T15:00:00+00:00

## Installation

1.  Place the `timenow` script in a directory that is in your system's `PATH` (e.g., `/usr/local/bin`).
    ```bash
    sudo mv timenow /usr/local/bin/timenow
    ```
2.  Ensure it is executable.
    ```bash
    sudo chmod +x /usr/local/bin/timenow
    ```