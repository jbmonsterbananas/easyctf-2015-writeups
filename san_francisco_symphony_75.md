# San Francisco Symphony (75)

## Problem

Who knew musicians could program? They put a flag inside `/problems/sfs/sfs`! But when I run the program, it's not printing out the flag. Find the flag!

## Hint

Darn. That `c` file isn't going to help much either. How can we find the flag using only the binary?

## Write-Up

Navigate to `/problems/sfs` to figure out what to do first. List the files in the directory with `ls`
If you try to do `cat sfs.c`, you'll get permission denied, so instead follow the hint and open sfs with `cat sfs`.

After all the binary loads, scroll up and get your flag.

flag = `easyctf{w0aw_stor1ng_fl4gs_in_pla1nt3xt_i5_s0oper_s3cure}`