# Known Plaintext 3 (300)

## Problem

Solve the problem using the programming interface. The input file is `knownplaintext3.in`.

The input is formatted `[d/e] <string>`. The first character specifies whether the assignment is to encrypt or to decrypt, and the string is either the plaintext or the ciphertext, depending on the first letter.

## Hint

Figure it out yourself ;)

## Write-Up

After running some test cases a couple of time, you I noticed that it was a simple substitution cipher.
I ran it enough times to translate every letter and wrote code based on that.

```python

def decode(chars):
	ans = ""
	b = list("ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz")
	a = list("CWKygzGDOIVBLnQqpmHtfJxYoShvMREeFwdTNuAcilakZUrXsbjP")
	for i in range(0,len(chars)):
		ans += b[a.index(chars[i])]
	return ans

def encode(chars):
	ans = ""
	a = list("ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz")
	b = list("CWKygzGDOIVBLnQqpmHtfJxYoShvMREeFwdTNuAcilakZUrXsbjP")
	for i in range(0,len(chars)):
		ans += b[a.index(chars[i])]
	return ans

reader = open("knownplaintext3.in", "r")
line = reader.read()
mode = line[0:1]
text = line[2:len(line)]
chars = list(text)

ans = "NOTHING"
if mode == "e":
	ans = encode(chars)
else:
	ans = decode(chars)
	
printer = open("knownplaintext3.out", "w")
printer.write(ans)

```

flag = `easyctf{at_least_im_better_than_caesar}`
