# Steganography-for-CTFs

So in stegnography FOR CTF's data is hidden in form of 
- Image
- Audio Files

- To solve such challenegs there are various tools and techniques we resolve them as
step by step check but before we do that the tools can be manually downloaded or 
can use the repo also [Toolkit](https://github.com/DominicBreuker/stego-toolkit)

## Easy Challenges
+ [ ] Check File type               
> file image.png
+ [ ] Check Strings in file         
> strings image.png || grep flag or something related
+ [ ] Check Metadata via exiftool   
> exiftool image.png  [Exiftool Commands](https://ninedegreesbelow.com/photography/exiftool-commands.html)
+ [ ] Check zipped/compressed data  
> binwalk -e image.png  
+ [ ] Check hidden data embeded     
> There are two methods
* 1) You know password - steghide extract -sf image.png 
* 2) Dont know password - stegcracker image.png
+ [ ] Check broken image header     
> hexedit image.png  
* a normal png header is ```00000000  89 50 4e 47 0d 0a 1a 0a  00 00 00 0d 49 48 44 52  |.PNG........IHDR|```
* a JFIF header is       ``` 0x FF D8 FF E0 xx xx 4A 46 49 46 00 ```   

+ [ ] Check Hidden between Images   
> zsteg image.png
+ [ ] Check for text file           
> A txt file is given with paragraphs here stegsnow might help to retrive flag
+ [ ] Check for Spectrogram         
> mp3 wav file you can use audacity
+ [ ] Check data in LSB/MSB/Xth Bit 
> [SHIT](https://github.com/qll/shit) 

## Medium Challenges
