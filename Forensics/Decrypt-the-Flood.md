# Decrypt the Flood

### Description: Dive into the digital currents of Decrypt the Flood! Navigate through encrypted waters, uncovering clues hidden within the network flow. Will you decrypt the mystery behind Anthony's vanished invention, or will it remain lost in the flood?

We are given a pcap. 

-> Wireshark

<picture>
  <img src="https://github.com/Befoul-Writeups/RITSEC24Warmups/blob/main/Forensics/wiresh.png">
</picture>
We see that its a SYN flood

First thing I try is Ctrl+F and look for the beginning of the flag format "RS{"

<picture>
  <img src="https://github.com/Befoul-Writeups/RITSEC24Warmups/blob/main/Forensics/wiresh2.png">
</picture>

Flag: RS{pc@p$_@r3_0ur_fr!3nd$}
