# Gobustme ?
## artifacts
<a href="https://gobustme.ctflearn.com/">https://gobustme.ctflearn.com/</a> <\n>
<a href="https://www.securitynewspaper.com/2019/11/04/bruteforce-any-website-with-gobuster-step-by-step-guide/">securitynewspaper.com/2019/11/04/bruteforce-any-website-with-gobuster-step-by-step-guide/</a> <\n>
<a href="https://raw.githubusercontent.com/v0re/dirb/master/wordlists/common.txt">https://raw.githubusercontent.com/v0re/dirb/master/wordlists/common.txt</a>
## process
### step-01
The author has so kindly provided us with everything we need to know. So I follow the guide to use Gobuster: first install it in my kali virtual machine, and then download the `.txt` file as `commonbrute.txt`(this is optional, I was just lazy to type)
### step-02 
Craft the command as taught in the guide. I wrote mine like so: `$ gobuster dir -u https://gobustme.ctflearn.com -w commonbrute.txt`
### step-03
you need to wait a little for the results as there are 4000 something words to go through. But anyway, after it's done, you should see a list of directories that gobuster has found. Just test through every single one of them. And you could test the incorrect links just for the lols, it's funny :)
![image](https://github.com/functionpdf/CTFlearn/assets/102633295/57e64f8c-3e1b-47f8-b6f0-7cf4b5fb1aa1)
## flag
`CTFlearn{gh0sbu5t3rs_4ever}`
