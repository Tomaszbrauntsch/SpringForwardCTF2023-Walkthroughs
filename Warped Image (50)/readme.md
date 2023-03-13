# Warped Image (50 points)

## Challenge
![challenge](https://user-images.githubusercontent.com/43079538/224836152-d2eb1e6e-e256-4fb0-bc9d-dfdf7cebf0ea.png)
<br>
![hint](https://user-images.githubusercontent.com/43079538/224836170-a4f85978-efed-4c0b-a18d-443e18b0d310.png)

We are given a jpg file called Image2.jpg. I took note of:
<br>
*no longer can see the file*
<br>
*restore image with magic*
<br>
<br>
<br>
<br>
The first thing I thought of using is magic in [cyberchef](https://gchq.github.io/CyberChef/) but it result in nothing. I tried to extract with EXIF data (since we had to do it in Say Cheese!, it may have some good information) and it displays with an error.
<br>
![cyberchef](https://user-images.githubusercontent.com/43079538/224836631-97d141fc-fca8-45bb-84ae-4147133468d8.png)
<br>
<br>
<br>
Searching up "*magic file*" mentions something called *magic numbers*
<br>
![googlesearch](https://user-images.githubusercontent.com/43079538/224836446-ac275566-daa0-4cf4-b8cb-b33296dffbb0.png)
<br>
<br>
<br>
Searching up what magic numbers is, it gives us a [wikipedia article](https://en.wikipedia.org/wiki/Magic_number_(programming)) that has a section about magic numbers in files. Reading more into this section it gives us examples, one of these examples are on JPEG files
<br>
![magicnum](https://user-images.githubusercontent.com/43079538/224836673-4d9efcd0-26bc-4a0f-a306-4b540c467ae1.png)
<br>
I took note of the highlighted areas in the image above.
<br>
<br>
<br>
Using the command ```xxd Image2.jpg | less ``` it allows me to look at the first most line and the bottom most line via hexadecimal. The problem is in the first line of file
<br>
![xxdimage](https://user-images.githubusercontent.com/43079538/224835884-6ccccf13-5037-443e-918d-d1d1ecc63791.png)
<br>
Changing the highlighted bit from EF D8 to FF D8 using a hex editor tool (like hexedit on unix, using [vim](https://transang.me/edit-binary-file-with-vim-and-the-xxd-command/), or HxD on windows), it allows for the image to be viewable and when opened gives us flag.
<br>
<br>
![flag](https://user-images.githubusercontent.com/43079538/224835830-4c54c4e4-509a-4dca-b4c0-542df18ba64e.jpg)
<br>
```nicc{F0rensics_M@gic_Byt3$!}```
