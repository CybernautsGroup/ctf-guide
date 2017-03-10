## Crypto

### Caesar Cipher / Rot13

Read about the Caesar Cipher here: [https://en.wikipedia.org/wiki/Caesar\_cipher](https://en.wikipedia.org/wiki/Caesar_cipher)

If you ever see text that looks something like this: "ftue xaawe egebuouage". You should always test to see if it is a rot\(n\).

All the `rot(n)` can be deciphered here:

\[[https://kt.pe/tools.html\#conv/\]\(https://kt.pe/tools.html\#conv/\](https://kt.pe/tools.html#conv/]%28https://kt.pe/tools.html#conv/%29\)

This is a pretty crappy script that also does all the rots. But only with lower case letters.

```py
import sys

message = sys.argv[1].lower()
splitted = list(message)

for num in range(26):
  result = []
  for char in splitted:
    if char.isalpha():
      charNum = ord(char)
      # 122 because that is "z" in the ascii-table
      if charNum + num > 122:
        # 96 because that is "a" in the ascii-table
        char = chr(96 + ((charNum + num) - 122))
        result.append(char)
      else :
        result.append(chr(charNum + num))
    else:
      result.append(char)

  print "Rot" + str(num) +": " + "".join(result)
```

# Vigenère cipher {#firstHeading}

This cipher-text will, just like caesar cipher, look like a sentence.

You can use \[this\]\([https://www.guballa.de/vigenere-solver\](https://www.guballa.de/vigenere-solver%29\) site to decipher the Gienére cipher.

## XOR cipher

With the help of xor we can encrypt stuff.

Here is a good explanation of who it works.

[https://en.wikipedia.org/wiki/XOR\_cipher](https://en.wikipedia.org/wiki/XOR_cipher)

## Substitution cipher

[https://en.wikipedia.org/wiki/Substitution\_cipher](https://en.wikipedia.org/wiki/Substitution_cipher)







