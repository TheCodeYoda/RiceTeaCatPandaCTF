This challenge was a basic reverse challenge for 300 points.Runnning "FILE" command on this revealed that it was a 64-bit ELF executable with PIE enabled,so even if we wanted to use GDB it would require a single session.Running the executable asks a password, entering the correct one would spit out the flag.Running "strings" on it was not so useful.The next step would be to open this file using a decompiler(IDA or GHIDRA), in my case I used GHIDRA.
After locating the main function(offset:0x7c0) the code was displayed in this fashion..

![mainfxn](https://user-images.githubusercontent.com/46860321/73137023-12927f80-407a-11ea-864a-868848a6af02.png)


Analysing the main function we can see that it performs some kind of xor operation on our input and compares it with DAT_00301020 if we can reverse that particular operation and apply it on DAT_00301020 we can get the password. Observing the code we see that its taking character at &DAT_00301020 i steps of 50.

![offsets](https://user-images.githubusercontent.com/46860321/73137028-16260680-407a-11ea-8b39-a6081b873cde.png)

first hex byte is 0x3a after jumping 50 addresses we get the next hexbyte.The array of hexbytes are specified in the python script.The python script also has the details of the reverse operation to be performed.After running the python script the password we get is:

"50m371m32_5Pr34D_0U7"

entering this we get the flag:

rtcp{fL492_r_50m371m32_5Pr34D_0U7}
