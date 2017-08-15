# proteus
A command-line program for detecting, decoding, and converting radix-encoded strings.

This program is meant to be used with the most popular base-encodings such
as base64, hexadecimal, binary, etc. Also the encodings are expected to
be in their most commonly used implementation of each respective radix.

     Example: uuencode will not work (no use of lower-case), nor will BinHex4,
              otherwise known as HQX because they use a different 64 character
              set. 
              
These could be implemented using the binascii.a2b/b2a uu and hqx functions.

Furthermore, the program largely operates under the assumption of ASCII
being in UTF-8 (8-bit unicode).





# refactoring

These are areas of the script that, while functional, are in need of refactoring.

             - Encoding detection
             - Binary<-->ASCII conversion (some benchmarking is needed here)
             - Radix to Radix conversion in general (current method is Radix->ASCII->Radix)




# development

These are parts of the program that are either half-implemented or broken in their current form.

             - Support for Base85
             - Setting output width (useful for encodings like Octal that require breaks)



# future implementation

These are the plans for added functionality in future versions. 

             - File support (reading/writing without need for command line redirection)
             
             - Detection support for uuencoding (only detection)
             - Support for Base36
             - Support for NewBase60
             - Support for derivatives of Base64 (Base52, Base57, Base58, Base62, Base65)
             - Support for Hexavigesimal (Base26)
             - Support for post-Unnonagesimals (Base91-Base95)

             - GUI front-end(s) (e.g. GTK)
             
# background

Lately (due to playing some 'Alice & Smith' augmented-reality games), I've been finding it necessary to do radix conversions (usually just into ASCII format). It appears everyone's main goto are online web-tools. However, I was surprised there wasn't a do-it-all program already available in Linux. Sure, there's binuntils, but nothing sleek and "comprehensive". I always wanted something that would be able to auto-detect a format. I wanted something simple, fast, yet powerful. So I wrote Proteus: "the totally radixcal script". 

I used to write cryptanalysis tools in the past using Python, particularly for language detection scoring (for obvious reasons). So I thought it would be fun to write this tool in Python as well in the spirit of fun. This also had the added benefit of making proteus cross-platform.

As for the name proteus, I chose it because it is the name given to a deity in Greek Mythology, also referred to as the "Old Man of the Sea". The god was known for his mutability, and I felt this matched well with a script that morphs strings, yet ultimately the body or meaning remain the same. 
