import string
def caesar(alphabet, strings, decode = False):
   if decode: strings = 26 - strings
   return alphabet.translate(
       string.maketrans(
           string.ascii_uppercase + string.ascii_lowercase,
           string.ascii_uppercase[strings:] + string.ascii_uppercase[:strings] +
           string.ascii_lowercase[strings:] + string.ascii_lowercase[:strings]
           )
       )
msg = "Wow how fun is it?"
print msg
enc = caesar(msg, 11)
print enc
