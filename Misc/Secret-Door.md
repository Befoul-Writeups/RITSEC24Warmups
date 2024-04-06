# Secret Door

### Description: You have found a secret door, to unlock it you must analyze the circuit design to obtain the code.

<picture>
 <img src="https://github.com/Befoul-Writeups/RITSEC24Warmups/blob/main/Misc/misc.png">
</picture>

I recreated the diagram using https://circuitverse.org/simulator 

After recreating the diagram, I found that the only way to get an output was by setting the following input values 0 1 0 0 0 1 1 1 (from 0 to 7)

Flag: RS{01000111}
