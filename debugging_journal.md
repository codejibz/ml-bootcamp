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

### Not a Bug per se, but equally as important
- **Symptom:** Dict comprehension produced fewer entries than expected.
- **Cause:** Duplicate keys silently overwrite — last assignment wins.
- **How I'd find it:** Compare len(my_dict) to the length of the input list. If they differ, you have duplicate keys.
- That len() check is genuinely how one would catch it in real code. Cheap, fast, and most beginners forget to do it.

## Day 1 — ...

### Bug 1

- Symptom: Added if len(values) > 0 else 0 guard in the mean calculation.
- Cause: The guarded case was unreachable — keys only enter numeric_values when a value is appended, so the list is never empty at that point.
- How I found it: Mentor asked "can this branch actually execute?" — traced back and confirmed no path leads to it.

Pattern noticed: defensive guards (if len > 0 else 0) added without checking whether the guarded case is reachable. The case wasn't reachable — keys only enter numeric_values when a value is appended. 
Future rule: before adding a guard, ask "can this branch execute?" If no, don't guard.

