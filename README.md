# Dell XPS 15 - 9560-OSX
This contains my modified files to run OS X 10.12.3, based on Andy^^s collection and my tutorial for the 9550.

You can follow my guide if you want to install Sierra on your own dell, but be aware, the tutorial is originally for the 9550.  
Best way is to download the 9550 repository and then overwrite the files with the ones from this repository.  

Link: [Dell 9550 Sierra Installation Guide][1].  
    
Not working:
* Wifi (will never work, replacement required - [my suggestion][2])
* nVidia GPU (Intel IGF works well)
* SD Card reader

## Firmware Update
These files are only suitable for Firmware Version 1.3.0 or below. If you run a newer firmware, you may have to delete CLOVER/drivers64EFI/OSXAptioDrv-64.efi and replace it with OSXAptioDrv2-64.efi and add a customized slide to the boot arguments (for example slide=168 or slide=170). [Tutorial on how to calculate your slide parameter][3]  

## Step 1:
Download the files from the repository for the XPS 9550:  
```
git clone https://github.com/wmchris/DellXPS15-9550-OSX -b 10.12-BIOS1.2.21
```

## Step 2:
Download the "patch" for the XPS 9560:  
`git clone https://github.com/wmchris/DellXPS15-9560-OSX`

## Step 3:
replace all files from Step 1 with their supplied counterparts from Step 2. Make sure to overwrite supplied files and to merge the folders.
```
rsync -avh --progress ./DellXPS15-9560-OSX/ ./DellXPS15-9550-OSX/
rm -Rf ./DellXPS15-9560-OSX
mv DellXPS15-9550-OSX DellXPS15-9560-OSX
```
## Step 4:
follow the [original 9550 tutorial][1], but ignore the part with the ig-platform-id.   
https://github.com/wmchris/DellXPS15-9550-OSX/blob/master/Tutorial_10.12.md

[1]:  https://github.com/wmchris/DellXPS15-9550-OSX/blob/master/Tutorial_10.12.md
[2]:  https://wikidevi.com/wiki/Dell_Wireless_1830_(DW1830)
[3]:  https://github.com/wmchris/DellXPS15-9550-OSX/blob/master/Additional/slide_calc.md
