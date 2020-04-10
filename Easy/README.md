
# Easy 
In these type of challenges the file mostly used are
- Image
- Audio Files

## Now Lets look at how challenges look like

### 1. Adding strings inside a file
In such challenges a normal looking image or file would 
be present and some strings would be inserted inside it.
They are generally being added at end of file also if not
 you can grep for it using particular keywords
#### To Solve:
You can use string/cat commands to check 
> strings image.png |grep flag or something related

### 2. Modifying file type 
In such challenges the image is either made corrupted,its
format is changed, renamed or headers are modified.

- a)Header changed
A normal PNG file header would look like 
```00000000  89 50 4e 47 0d 0a 1a 0a  00 00 00 0d 49 48 44 52  |.PNG........IHDR|```
now it would be broken and changed as
```00000000  89 00 00 00 00 0a 1a 0a  00 00 00 0d 49 48 44 52  |............IHDR|```

- b) Renamed 
In such challenges a normal file would be renamed to something else and we would need
to find whatr actually file is and rename accordingly


#### To Solve:
a)First you need to decide what orignal fight might be like jpeg,gif,qr code etc then
you can use hedxedit/hexeditor to manually change the headers to required file format
then you can obtain the orignal file

b)First find what orignal image was by typing 
``` file given.extension```
now on basis of result rename it


### 3. Compressing/Embeding data in a image
Data is hidden inside our orignal file which either might be embeded
or zipped inside it 

- a)Zipped 
Here the file which you got can be unzipped/extracted and
would give you a new file which might be your flag.In such
cases 

- b) Embeded
Here a file would be attached but in order to recover it you might need
a password for it or it may be blank.We can use steghide in order to 
embed/extract a file from another file

#### To Solve:
- a)Check zipped/compressed data
binwalk -e image.png

- b)Check hidden data embeded
There are two methods

You know password - steghide extract -sf image.png
Dont know password - stegcracker image.png

















