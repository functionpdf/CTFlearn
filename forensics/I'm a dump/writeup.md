# I'm a dump

## artifacts
![file](https://github.com/functionpdf/CTFlearn/edit/main/forensics/I'm%20a%20dump/file)

## process
### step-1
Any hints? Even though I'm relatively new to CTFs, I can still spot the hint in the title. 'Dump' probably refers to Hexdump. The problem description also mentions hexadecimal. Ok, let's put it into Cyberchef. `Magic` doesn't seem to do anything. 
### step-2
Nevermind, `From Hexdump` doesn't seem to do anything, nor does `From Hex`. 
### step-3
How about `ctrl f`? And I find something that resembles a flag in plain site with no recipe. `CTFlearnHº{fl4ggyfHEÐHUØHÇEàl4g}' isn't the correct flag though. 
### step-4
the problem description tells me to `removing an useless H.E.H.U.H.E. from the flag`. I have no idea what that means, let's just remove all the special characters from the flag and see what happens. 
### step-5
Doing that gave me `CTFlearn{fl4ggyfHEHUHEl4g}`, which isn't the flag. But I guess I forgot to remove the `HEHUHE`?

## flag
`CTFlearn{fl4ggyfl4g}`
