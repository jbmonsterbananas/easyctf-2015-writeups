# Same Difference (125)

## Problem

*Solve this problem by connecting to the EasyCTF shell, either in your browser or through some other TTY.*

We've noticed that a list of passwords has been modified. Compare the original `master_copy.txt` to the `suspicious.txt` and tell us what the password was changed to! The files are on the shell server at `/problems/same_difference`.

This can be solved only with the tools available in the shell. No scripting languages are required.

## Hint

There's a pretty cool Linux command called `diff` that might be useful for you.

## Write-Up

After navigating to the folder, and looking up `diff`, we use it on the two files and get this:

```
$ diff master_copy.txt suspicious.txt
8834c8834
< easyctf{17c85a939e5ee1b0b0e00ed7187d11f7}
---
> easyctf{60a57b3974029aa012e66b05f122748b}
```

flag = `easyctf{17c85a939e5ee1b0b0e00ed7187d11f7}`