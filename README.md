# Dell XPS 15 - 9560-OSX
This contains my modified files to run OS X 10.12.3, based on Andy^^s collection and my tutorial for the 9550.

You can follow my guide if you want to install Sierra on your own dell, but be aware, the tutorial is for the 9550. You need to adapt many of the steps with the files supplied in this repository. Link: [guide][1].  
  
Some hints: you need two config.plist, one for installation and one for general usage. They only differ in FakeID: IntelGFX set to 0x12345678 for installation.  
  
Not working:
* Wifi (will never work, replacement required)
* nVidia GPU (Intel IGF works well)

[1]:  https://github.com/wmchris/DellXPS15-9550-OSX/blob/master/Tutorial_10.12.md
