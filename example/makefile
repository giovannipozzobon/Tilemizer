
KICK = java -jar /Applications/KickAssembler/KickAss_5.21.jar -vicesymbols -showmem  -bytedump

all: 16colortilemode.prg 


16colortilemode.prg: 16colortilemode.s
	python3 ../tools/tilemizer.py -m=8000 -b4 -o=data/grid -t=data/grid.bmp
	$(KICK) 16colortilemode.s

run: 16colortilemode.prg
	../tools/m65.exe -l COM6 -F -r 16colortilemode.prg

clean:
	rm 16colortilemode.prg 
	rm data/grid.map 
	rm data/grid.chrs 
	rm data/grid.atr
