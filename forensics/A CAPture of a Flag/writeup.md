# A CAPture of a Flag
## artifacts
<a href="https://github.com/functionpdf/CTFlearn/blob/main/forensics/A%20CAPture%20of%20a%20Flag/flag.pcap">flag.pcap</a>
## process
### step-01
From the problem statement, we can see the keywords `wireshark` and `capture`. This seems to suggest that the `flag` file should be a network packet. Let's change the file extension to that and open it in Wireshark
### step-02
It's inane to sift through hundreds of packets with your eyes. But there is a way to filter all this data. I thought maybe I should filter by HTTP because data can be transferred through it(duh). And there we go.
<img src="https://github.com/functionpdf/CTFlearn/assets/102633295/5397136e-ae4a-46a3-8fdc-060ef96f1495">
### step-03
This looks like base-64, so I plugged it into Cyberchef and got the flag.
## flag
`flag{AFlagInPCAP}`
