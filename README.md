# Hey

A tiny shell script for quick, directory-specific note-taking in your terminal.

## The Why

In a developer's workflow, context is everything. Jumping from the terminal to a separate application like Notepad, Notion, or a to-do list to jot down a thought seems simple, but it breaks your flow. You lose your mental state, your "train of thought," and getting back into the zone takes time and energy.

`hey` is built to combat this context switching. It's for developers who live in the terminal and want a frictionless way to capture thoughts, track progress, or make a quick note without ever leaving the command line. It keeps your notes where you work, right alongside your code.

## Use Cases

*   **Task Tracking:** Keep a running log of what you've completed in a project. Quotes are optional. Don't include more than one set of quotes.
    ```bash
    hey 'Finished setting up the database schema'
    hey 'Fixed the authentication bug #123'
    hey  Just added expenses to xero for march 
    ```
*   **Work Journal:** Maintain a daily work log for reporting or personal tracking.
    ```bash
    hey 'Starting work on the new feature'
    hey 'Meeting with the design team'
    ```
*   **Quick Notes:** Jot down ideas, commands, or reminders without breaking your stride.
    ```bash
    hey 'Remember to check the server logs for errors'
    hey '`npm install -D tailwindcss`'
    ```

## How It Works

`hey` saves your notes to a `timelog.md` file. By default, it creates this file in your **current working directory**. This means your notes for different projects never get mixed up. It's a quick, dirty, and effective way to keep track of what you're doing, right where you're doing it.

## Usage

### Log a timestamp
```bash
hey
```
> Logged to ./timelog.md: 23:00:00 25-11-14

### Log a timestamp with a comment
```bash
hey "Finished refactoring the auth module"
```
> Logged to ./timelog.md: 23:01:00 25-11-14 - Finished refactoring the auth module

### List the last 10 entries
You can use `list`, `ls`, or `whatsup`.
```bash
hey ls
```
> ---
> Showing last 10 entries from ./timelog.md:
> ---
> * 23:01:00 25-11-14 - Finished refactoring the auth module
> * 23:00:00 25-11-14

## Installation

There are two ways to use `hey`:

### 1. Global (Recommended)

This allows you to run `hey` from any directory, and it will create a `timelog.md` in that directory.

1.  Copy the `hey` script to a directory in your system's `PATH`.
    ```bash
    sudo cp hey /usr/local/bin/
    ```
2.  Make it executable.
    ```bash
    sudo chmod +x /usr/local/bin/hey
    ```

### 2. Per-Project

If you prefer to keep the script within each project:

1.  Copy the `hey` script to your project directory.
2.  Make it executable (`chmod +x hey`).
3.  Run it using `./hey`.

### 1. Make it better
1.  Maybe youc could extend it by logging where a timelog.md is when it is created ina global file then run reports or a markdown based kanban off it.
2.  Maybe you could add numbering and then add a command hey 10 done or hey 10 doing or hey 10 WaitingFor to give them simple status
3.  Maybe add tags
4.  Maybe nothing. keep it simple
