# scratch-lang-docs
Documentation for ScratchLang

# How to add more blocks to the decompiler
Adding more blocks to ScratchLang is a simple process.

But first, you must know how the program reads the .json.
There are some common functions that the script uses.

```py
def getchar(a1, a2=""): # This function gets character i of the project.json file. If the first characters of the project. Let's say the first characters of the file are "abc." If i is 0, then the char variable will be a. If i is 1, then it will be b, .etc. The argument a1 is the character it's looking for. If character i of the json equals the value of a1, then it will return 1. If not, return nothing.
    global b
    global char
    b = ""     
    if not "-" + a2 == "-++": # If the value of a2 is ++, then get the character i + 1. Don't use this one.
        char=jsonfile[i] # Sets the variable char to letter i of the project.json.
        if "-" + char == a1:
            b = "1"
    elif not "-" + char == a1:
        char=jsonfile[i + 1] # Sets the variable char to letter i + 1 of the project.json.
        if "-" + char == a1:
            b = "1"
        char=jsonfile[i] # Sets the variable char to letter i of the project.json.
    else:
        char = ""
    return b
```