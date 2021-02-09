# Mega65
Utils and samples for Mega65

# Tilemizer

python script to convert images to tile,color,and map data.

REQUIRES https://pillow.readthedocs.io/en/stable/ to be installed.

will detect x&y flipped tiles and remove duplicated tiles. 
```
python tools\tilemizers.py 
options 
	-b4		set output to 4bpp 16 color mode 
	-b8		set output to 8bpp 256 color mode
	-m=ffffff set memory address tiles will be in memory ( to offset map data ) 
	-o=<outputprefix>	output files will be
				outputprefix.chrs ( tile data )
				outputprefix.clut ( color data )
				outputprefix.map ( screen data )
				outputprefix.atr ( color/attribute data )
				outputprefix.info ( width and height of map data )
	-t=<inputfile>		will convert specified image into Mega65 tiles and output the data

	soon 
	-s=<inputfile>		sprites
```

# e.g.
python tools\tilemizer.py -m=c000 -b4 -o=data\mega -t=data\mega.bmp

# notes 

	We assume that the 1st 16 colors of the input image is palette 0 . 2nd 16 colors is palette 1 etc. 
	no image quantization is performed. 


# Examples

#	16colortilemode.s 

	Sets up 16 color tile mode and uses data generated by tilemizer.

	locally we have kickassembler and m65. so you will need to adjust the makefile 





