# No Expectation of Privacy (50 points)

**NOTE** I don't think I solved this challenge as intended

## Challenge

## Hint

The only file that is provided with this challenge is a pcapng file. If you search up *how to open a pcapng file* it will point you to use wireshark. Wireshark is a tool used to analyze network packets that was sniffed. 

## Overview of the information displayed in Wireshark

Once you open the file you are provided with a bunch of random information.  Don't worry it isn't as bad as it looks. 
Column 1: Packet number; the order the packets came in while wireshark was sniffing for packets
Column 2: Time; At what time this packet was sniffed
Column 3: Source IP address
Column 4: Destination IP address
Column 5: Network Protocol that was used
Column 6: Length of the information in Info
Column 7: Information in the packet

The first thing to do is do search querys on *filtering packets in wireshark*, this will allow you to apply different conditions on the information to appeal to your liking. 
Since I knew the flag format was nicc{}, I used the following filter to find the keyword nicc in the info column. 
```frame contains "nicc"```

This presents you with a single packet and when double clicked presents you with the flag

nicc{th3y_t011_f0r_th33}
