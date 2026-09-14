# Windows Sysmon Event ID 1 – Process Creation

## Overview

Sysmon Event ID 1 records process creation activity on a Windows system.

SOC analysts use this event to understand which process started another process and what command was executed.

---

## Important Fields

When analyzing Event ID 1, I focus on:

- **Image** – The process that was created
- **CommandLine** – The command executed
- **ParentImage** – The process that started the new process
- **ParentCommandLine** – Command used by the parent process
- **User** – Account that executed the process
- **Hashes** – Useful for identifying suspicious files
- **Timestamp** – When the activity occurred
- **Host** – System where the activity occurred

---

## Parent-Child Process Relationship

A parent process starts a child process.

### Example 1 – Likely Legitimate Activity

**Event ID:** 1  
**Parent Process:** `explorer.exe`  
**Child Process:** `cmd.exe`  
**Command Line:** `cmd.exe /c ipconfig`

#### Analysis

- `explorer.exe` is a normal Windows process.
- `cmd.exe` is a legitimate Windows command interpreter.
- `ipconfig` is a normal networking command.
- There are no obvious suspicious indicators.

**Verdict: Likely Legitimate**

Example:

```text
explorer.exe
      |
      └── cmd.exe
