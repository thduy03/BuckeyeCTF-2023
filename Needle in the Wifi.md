## Needle in the Wifi

![enter image description here](https://i.imgur.com/gP0Rqhq.png)
### Solution
We received a file named `frames.pcap`. We can open it with Wireshark:
![image](https://github.com/thduy03/BuckeyeCTF-2023/assets/126741377/1acd9ec7-1b92-4d34-ab20-74c90b0256b4)


We can immediately see that there are a lot of packets containing the `SSID` encrypted in `base64`.  So the first thing we need to do is export all `SSID` values from all packets using `tshark` command: 
`tshark -r frames.pcap -T fields -e wlan.ssid > output.txt`

This is the file that contains all the `SSID` values:![enter image description here](https://i.imgur.com/zxwczde.png)

After decoding the file, we will find the flag:
![enter image description here](https://i.imgur.com/UUs3ms7.png)Flag:`bctf{tw0_po1nt_4_g33_c0ng3s7i0n}`
