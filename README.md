# Hey

A tiny shell script for quick, directory-specific note-taking in your terminal.

## The Problem

Your notes and todos should be where you are. If you spend your day in the terminal, you shouldn't have to leave it just to jot down a thought, track your progress, or note an idea.

## The Solution

`hey` is a simple script that lets you quickly capture timestamped notes without leaving your command line.

Because it saves notes to a `timelog.md` file **in your current working directory**, your notes for different projects never get mixed up. It's a quick, dirty, and effective way to keep track of what you're doing, right where you're doing it.

## Usage

### Log a timestamp
```bash
./hey
```
> Logged to ./timelog.md: 23:00:00 25-11-14

### Log a timestamp with a comment
```bash
./hey "Finished refactoring the auth module"
```
> Logged to ./timelog.md: 23:01:00 25-11-14 - Finished refactoring the auth module

### List the last 10 entries
You can use `list`, `ls`, or `whatsup`.
```bash
./hey ls
```
> ---
> Showing last 10 entries from ./timelog.md:
> ---
> * 23:01:00 25-11-14 - Finished refactoring the auth module
> * 23:00:00 25-11-14

## Installation

For per-project logging, the recommended approach is to place a copy of the `hey` script in each of your project directories.

1.  Copy the `hey` script to your project directory.
    ```bash
    cp /path/to/hey /path/to/your/project/
    ```
2.  From within your project directory, make it executable.
    ```bash
    chmod +x hey
    ```
3.  Run it using `./hey`.
