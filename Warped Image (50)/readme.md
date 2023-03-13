# Warped Image (50 points)

## Challenge

We are given a jpg file called Image2.jpg. I took note of:
<br>
*no longer can see the file*
*restore image with magic*

The first thing I thought of using is magic in [cyberchef](https://gchq.github.io/CyberChef/) but it result in nothing. I tried to extract with EXIF data (since we had to do it in Say Cheese!, it may have some good information) and it displays with an error.

Searching up "*magic file*" mentions something called magic numbers

Searching up what magic numbers is, it gives us a [wikipedia article](https://en.wikipedia.org/wiki/Magic_number_(programming)) that has a section about magic numbers in files. Reading more into this section it gives us examples, one of these examples are on JPEG files

I took note of the highlighted areas in the image above. Using the command ```xxd Image2.jpg | less ``` it allows me to look at the first most line and the bottom most line via hexadecimal. The problem is in the first line of file


Changing this bit from EF D8 to FF D8 using a hex editor tool (like hexedit on unix, using [vim](https://transang.me/edit-binary-file-with-vim-and-the-xxd-command/), or HxD on windows), it allows for the image to be viewable and when opened gives us flag.

```nicc{F0rensics_M@gic_Byt3$!}```