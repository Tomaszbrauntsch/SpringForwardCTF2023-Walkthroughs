# No Expectation of Privacy (50 points)

**NOTE** I don't think I solved this challenge as intended

## Challenge
![challenge](https://user-images.githubusercontent.com/43079538/224814133-3ac5a850-9a31-4c01-af56-dcc0d98b3e98.png)

![hint](https://user-images.githubusercontent.com/43079538/224814158-6085b785-7dc7-4bee-9957-695bd03cd81d.png)

The only file that is provided with this challenge is a pcapng file. If you search up *how to open a pcapng file* it will point you to use wireshark. Wireshark is a tool used to analyze network packets that was sniffed. 
<br>
<br>
<br>
## Overview of the information displayed in Wireshark
![packet-analyze](https://user-images.githubusercontent.com/43079538/224814216-f07f66ae-b6cf-4193-b1aa-e08773c6586b.png)
<br>
<br>
<br>
Once you open the file you are provided with a bunch of random information.  Don't worry it isn't as bad as it looks.
<br>
Column 1: Packet number; the order the packets came in while wireshark was sniffing for packets
<br>
Column 2: Time; At what time this packet was sniffed
<br>
Column 3: Source IP address
<br>
Column 4: Destination IP address
<br>
Column 5: Network Protocol that was used
<br>
Column 6: Length of the information in Info
<br>
Column 7: Information in the packet
<br>
<br>
<br>
The first thing to do is to search online for *filtering packets in wireshark*, this will allow you to apply different conditions on the information to appeal to your liking. 
Since I knew the flag format was nicc{}, I used the following filter to find the keyword nicc in the info column.
<br>
```frame contains "nicc"```

This filter presents you with a single packet and when double clicked, presents you with the flag
<br>
<br>
![thepacket](https://user-images.githubusercontent.com/43079538/224815083-e3baa40a-0698-4cc9-8882-47bb63bff69c.png)


nicc{th3y_t011_f0r_th33}
