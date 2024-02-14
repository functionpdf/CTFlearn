# Calculat3 M3
## artifacts
<a href="http://web.ctflearn.com/web7/">http://web.ctflearn.com/web7/</a>
## process
### step-01
There's a form. Let's punch in a random expression and see what is going on inside inspect.
### step-02
Nothing is happening inside html nor applications, so let's navigate to network. There, we can see the requests. If we open up `web7` we can see the form information being posted. There is only one attribute there: `expression: 8 + 3`.
### step-03
I'm pretty sure you could also do this in the browser but I couldn't figure out how to post(lol) so I opened up command prompt and posted form information using curl. Since the only payload the website will take would be `expression`, I trialed and errored for the correct command to inject. Finally, I came up with `curl -d "expression=;ls" http://web.ctflearn.com/web7/`.
## flag
`CTFlearn{watch_0ut_f0r_th3_m0ng00s3}`
