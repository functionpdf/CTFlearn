# POST practise
## artifacts
http://165.227.106.113/post.php
## process
### step-1
The first thing we see on the site is `This site takes POST data that you have not submitted!`. Let's open inspect. In the HTML file's body, we can see a comment: `username: admin | password: 71urlkufpsdnlkadsf`. Nice of them to include everything we need! But first, what can we even use to solve this?
### step-2
When I did this I had no idea what POST was, and googling 'how can i manually submit POST data?' didn't produce any useful results, so I went to the comments and realised that I needed to use curl. It's quite useful for many HTTP request problems, apparently! So I then went to look for a <a href="https://curl.se/docs/tutorial.html">curl tutorial.</a>
### step-3
We can POST data using the -d command. For now I'm on Windows so I open up command prompt and enter: `curl -d "username=admin&password=71urlkufpsdnlkadsf" http://165.227.106.113/post.php`. Voila!
## flag
`flag{p0st_d4t4_4ll_d4y}`
