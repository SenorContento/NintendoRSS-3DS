# Install Instructions

These instructions are 

This should eventually be automated by the Makefile, but for now you need to type these instructions manually.

Instructions
------------

#### For Linux
--------------------------------------------------------------------
1. Make sure you are in the project root directory (aka NintendoRSS-3DS).
--------------------------------------------------------------------
2. Type the command below.
3. make
--------------------------------------------------------------------
4. If you already have bannertool, skip to Step 11. Otherwise, goto Step 5.
--------------------------------------------------------------------
5. Type the commands below.
6. git clone https://github.com/Steveice10/bannertool.git
7. cd bannertool
8. git clone https://github.com/Steveice10/buildtools.git
9. make
10. cd ..
--------------------------------------------------------------------
11. Type the commands below.
12. bannertool/output/bannertool makebanner -i media/banner.png -a media/home-sound.wav -o media/banner.bnr
13. bannertool/output/bannertool makesmdh -s "Nintendo RSS" -l "Nintendo RSS" -p "SenorContento" -i media/icon.png  -o media/icon.icn
--------------------------------------------------------------------
14. If you already have makerom, goto Step 15, otherwise download it from [here](https://github.com/profi200/Project_CTR/releases)
--------------------------------------------------------------------
15. Type the command below.
16. makerom -f cia -o NintendoRSS.cia -DAPP_ENCRYPTED=false -rsf sample.rsf -target t -exefslogo -elf NintendoRSS-3DS.elf -icon media/icon.icn -banner media/banner.bnr
