# Cave Johnson (450)

## Problem

Welcome to [Small Hole Sciences](files/cave-johnson.txt).

(Since all of their budget was spent on moon rocks, they were only able to afford an old-fashioned Vigenere Cipher.)

## Hint

[Information](https://en.wikipedia.org/wiki/Vigenere_cipher) from a reputable source

## Write-Up

First of all, we know that the type of encryption is Vigenere.
But for Vigenere decryption, you need a key.

You can use an online tool to try to figure out a key for you, this one worked best for me:
http://www.mygeocachingprofile.com/codebreaker.vigenerecipher.aspx

All we care about is the end of this chunk of text, so we can look at the ending of the first result and just guess that the first word is "this", since the decrypted text says `ttis`. 

So now our plaintext is `ttis_is_aperpure_enh_we_tnyk_toa_much` and our key is `eaimorbacorsiammorongore`.

You may also have noticed that `aperpure` should actually be 'aperture'.
You can determine this by realizing that the name of the question is 'Cave Johnson'
https://en.wikipedia.org/wiki/Cave_Johnson_(Portal)

Now using another Vigenere tool:
http://rumkin.com/tools/cipher/vigenere-keyed.php
We can use the key we got from before and decrypt the original ciphertext's flag portion.
(I only used this website because it updates automatically)

Now shift the key until you get `ttis_is_aperpure_enh_we_tnyk_toa_much` again. After that, you can change the 2nd and 11th letter of the key to match "this_is_aperture".

All that's left to do is delete characters from the end of the key until the whol flag is readable.

flag = `this_is_aperture_and_we_talk_too_much`