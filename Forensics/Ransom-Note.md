# Ransom Note

### After the break-in to his lab Anthony found a suspicious new file on his desktop named README.txt. Anthony opened the file and found that it was a ransom demand from whomever stole his invention. Perhaps the contents of the ransom note contain a clue to the attacker's identity.

<br />
We are given the following README.txt file:

-----BEGIN BITCOIN SIGNED MESSAGE-----

Your invention has been taken.

If you ever want to see it again send 10 BTC to this address:



bc1qd7qtdayjnl382qmfl4tl4yaejuv5py0n3uwq6p



You have 3 days.

-----BEGIN BITCOIN SIGNATURE-----

H3zAMJyVW2j1+Y7A+w8wflZRUmggR+Sn532ZuAGtGLcxEERvymcPrtnXVkB+0mBqCUAb0AQwyPFJfGxvIeQDPpE=

-----END BITCOIN SIGNATURE-----
<br />
<br />


The address given is bc1qd7qtdayjnl382qmfl4tl4yaejuv5py0n3uwq6p

We can simply put the address into https://www.blockchain.com/explorer 

From there we can follow the trail of transactions

<picture>
  <img src="https://github.com/Befoul-Writeups/RITSEC24Warmups/blob/main/Reversing/btc.png">
</picture>

The bottom right transaction shows funds going to the given address, lets follow it.

<picture>
  <img src="https://github.com/Befoul-Writeups/RITSEC24Warmups/blob/main/Reversing/btc1.png">
</picture>
<br />

We can see the flag under 
Decoded OP_Return


RS{26f9c2fcdfe8e86804eb} 

