# Now You See Me, Now You Don't (75)

## Problem

Now you see me, now you don't? There's a file in `/problems/elusive`, but I can't seem to find it. Find it and print its contents!

## Hint

What are `hidden files` in Linux?

## Write-Up

Go to the shell and navigate to the folder `/problems/elusive`

If you didn't know already, Googling Linux commands will give you tons of options, `ls -a` is what did it for me.
That will give you the file name `.hidden_file`, type `cat .hidden_file` and get your flag.

flag = `easyctf{just_playing_h1de_and_seek_lel}`