# Digital Camouflage
## artifacts
<a href="https://github.com/functionpdf/CTFlearn/blob/main/forensics/Digital%20Camouflage/data.pcap">data.pcap</a>
## process
### step-01
Open the `.pcap` file. "PCAP files are data files created using a program. These files contain packet data of a network and are used to analyze the network characteristics."
I opened it on <a href="https://apackets.com/pcaps/flows">apackets</a>.
<img src="https://github.com/functionpdf/CTFlearn/assets/102633295/ecd66d9f-276a-4ed7-9927-abbfec9ef320)">
### step-02
The problem asks for a password. From hint 1 ` It looks like someone logged in with their password earlier. Where would log in data be located in a network capture?`, I think it should be in the HTML log.
### step-03
Here there are 4 `GET` requests and 1 `POST` request. 
<img src="https://github.com/functionpdf/CTFlearn/assets/102633295/53ff104c-27ce-4282-acc4-56041084f5c5">
Since we know that only `POST` can send information from the client to the server, let's open it up.
### step-04
```
POST /pages/main.html HTTP/1.1
Host: 8080
Accept:  text/html,application/xhtml+xml,application/xml;q=0.9*/*;q=0.8
Accept-Language:  en-US,en;q=0.5
Connection:  Keep-Alive
Content-Length:  43
Content-Type:  application/x-www-form-urlencoded
Referer: 8080/index.html
User-Agent: 44.0) Gecko/20100101 Firefox/44.0
userid=hardawayn&pswrd=UEFwZHNqUlRhZQ%3D%3D
HTTP/1.0 200 OK
Connection: close
Content-Type: text/html
Date:30 GMT
Server: BaseHTTP/0.3 Python/2.7.9
```
From here we can see the password and userid field. `pswrd=UEFwZHNqUlRhZQ%3D%3D`, this should be our password. 
### step-05
Let's paste that into Cyberchef and see what happens. The problem is slightly misleading; there's a difference between decrypting and decoding. This one seems to be urlencoded, seeing from the %3D%3D. So run it through that first and we get `UEFwZHNqUlRhZQ==`, then, using `From Base64` will produce the flag.
## flag
`PApdsjRTae`
