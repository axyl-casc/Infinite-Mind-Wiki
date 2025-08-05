---
title: "Setup Troubleshooting"
tags:
  - robocode
  - tutorial
  - cs
  - beginner
  - troubleshooting
---

> 🤔 Having trouble getting Robocode running? Use this guide to solve common setup issues.

## Robocode won't launch

- **Issue:** Double-clicking the app does nothing.
  **Fix:** Make sure the downloaded folder is fully extracted. On macOS, right-click and choose _Open_ the first time to bypass security prompts.
- **Issue:** Robocode GUI won't open due to an incorrect Java version.
  **Fix:** Point to Java 21 before launching Robocode:

  **macOS**

  ```bash
  export JAVA_HOME=$(/usr/libexec/java_home -v 21)
  export PATH=$JAVA_HOME/bin:$PATH
  ```

  **Windows**

  ```cmd
  set "JAVA_HOME=C:\Program Files\Java\jdk-21"
  set "PATH=%JAVA_HOME%\bin;%PATH%"
  ```

  These commands temporarily use the correct JDK for the current session.

## "java" or "javac" not found

- **Issue:** Terminal says `command not found`.
  **Fix:** Confirm the JDK is installed and in your PATH.
  - **Windows:** Open Command Prompt and run `where java`. If it reports nothing, reinstall the JDK and check "Set JAVA_HOME".
  - **macOS:** Run `/usr/libexec/java_home` in Terminal to verify. If missing, reinstall using `brew install temurin`.

## VS Code can't find the JDK

- **Issue:** Java files show errors or the Run button is missing.
  **Fix:** Install the **Extension Pack for Java** and restart VS Code. If problems persist, press `Ctrl+Shift+P`, search for _Java: Configure Java Runtime_, and ensure the JDK path points to your installation.

## Robocode can't see your robot

- **Issue:** Robocode opens but no robots appear.
  **Fix:** In Robocode go to **Config → Bot Root Directories…** and select the `robots` folder inside your project. Save and reopen the Battle view.

## Still stuck?

Ask an instructor or teammate for help — there's usually a quick fix!

---

## Navigation

⬅️ [Back: Setting Up Robocode](/robocode/Day-1/02_setting_up)
➡️ [Next: Hello World Program](/robocode/Day-1/03_hello_world)
