# My Favorite Flag

We are given the C code "checker.c" and the compiled code a.out

First, let's look at the code. 

<picture>
  <img alt="Shows C code." src="https://github.com/Befoul-Writeups/RITSEC24Warmups/blob/main/Reversing/checkerc.png">
</picture>

1. b a list of hexadecimals
2. s = "RS{0h_b0y,I_10v3_f4k3_fl4gs!}" a fake flag
3. lowercase "L" is the length input that we will provide
4. if the length of our input is less than the length of the fake flag, s, it will return "Nope! Try again:)"
5. if we put the fake flag as our input, response will be "why would i like a fake flag??"
6. XOR operation, output[(2*i) % l] = input[i] ^ b[i]. In this we can see that b is going to XOR with our input and that it will be = output[(2*i) % l
7. if output is not the same as s, it will return "Nope! Try again :)"

So its just an XOR of the fake flag and the hexadecimal list.

I did it in python:

    b = [0x0, 0x28, 0x13, 0x36, 0x11, 0x7a, 0x6e, 0x4, 0x6c, 0x55, 0x5f, 0x39, 0x4, 0x1d, 0x4e, 0x66, 0x6f, 0x6b, 0x42, 0x49, 0x0, 0x52, 0x0, 0x53, 0x1f, 0x0, 0x56, 0x4e, 0x5c]

    output="RS{0h_b0y,I_10v3_f4k3_fl4gs!}"

    x = []

    for i in range(len(output)):

      x.append(ord(output[2*i % len(output)]) ^ b[i])
    
    print(x)

We get that the result of fakeflag XOR hexadecimals is 

x = [82, 83, 123, 84, 104, 51, 95, 114, 51, 97, 108, 95, 48, 110, 51, 53, 95, 52, 114, 101, 95, 98, 51, 53, 116, 95, 58, 41, 125]

from there we just need to turn this list into ascii

In python:

    flag = []

    for nums in x:

      flag.append(x)
      
    print(''.join(flag))


RS{Th3_r3al_0n35_4re_b35t_:)}   
