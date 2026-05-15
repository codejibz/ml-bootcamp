# Debugging Journal

## Day 0 — Environment Setup

### Bug 1
- **Symptom:** `code .` gave "zsh: command not found: code"
- **Cause:** VS Code's CLI tool wasn't added to PATH during installation
- **How I found it:** Command failed immediately; recognized it as a PATH issue
- **Fix:** ⌘+Shift+P → "Shell Command: Install 'code' command in PATH"

### Bug 2
- **Symptom:** After turning off conda auto-activation, Python version changed from 3.12.7 to 3.14.2
- **Cause:** Two separate Python installations on the machine; Anaconda's was winning via PATH, python.org's took over when conda deactivated
- **How I found it:** Ran `which python3` after the version change appeared
- **Fix:** Reference Anaconda's Python directly via full path when creating venvs

