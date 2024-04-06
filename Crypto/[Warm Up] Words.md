# Crypto [Warm Up] Words

We are given a jpg 

<picture>
  <img alt="pigpen cipher." src="https://github.com/Befoul-Writeups/RITSEC24Warmups/blob/main/Crypto/image.jpg">
</picture>

(I had no idea what this was originally)

So, I took it to an online stegnography tool I know, https://www.aperisolve.com/

Putting the image through it tells us that the common passwords are TIMEISOFTHEESSENCE, Ydnas, timeisoftheessence.

There was not much useful information beyond that.

Then I decided to ask gpt about the description of the challenge, "X marks the spot, but not where the Pigpen lies; there, secrets hide in plain sight." Gpt confirmed that this could be related to pigpencipher

We can use https://www.dcode.fr/pigpen-cipher for this. 

After deciphering we get that the code says TIME IS OF THE ESSENCE.

Flag: RS{TIME_IS_OF_THE_ESSENCE}

the flag was not case sensitive and the spaces were underscores, this was mentioned in the announcements. 
