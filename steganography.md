## Steganography

Steganography is the practice of hiding messages in different types of media. In CTFs that usually means flags hidden in images, video or sound files.

There are three main methods of hiding information via steganography:

* Injection
* Substitution
* File Generation

**Injection:**

The hidden information is injected into unused areas of a file. For example, comments in an image or sound file, particular html tags, or white space in a document. The main downside to injection steganography is that it increases the size of the base file, sometimes quite significantly.

**Substitution**

This is the most common method seen in CTFs. Information is substituted in place of existing data. The benefit of substitution steganography is that the file size remains the same. The most common substitution technique involves the Least Significant Bit method \(LSB\). In a graphic file, color codes usually use 8 bits, but the human eye can only distinguish between 6 bits of color information. The remaining 2 bits can be replaced with the hidden information with very little discernible difference.

**File Creation**

There are many tools that can create a new file containing the hidden information. The secret input is actually used to create the output file, typically in the format of a fractal image or even readable text.

**Tools**

Stegsecret

Stegspose

Image Steganography

Hyden- Hide steganographic data in an executable

Spammimic- Hide a message inside a spam email



