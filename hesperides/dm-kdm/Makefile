#!/usr/bin/make -f

include ../theme-control.make

BITMAPS = files background fred

all: $(BITMAPS)

files:
	mkdir -p $(THEME)
	cp session.png $(THEME)
	cp system.png $(THEME)
	cp KdmGreeterTheme.desktop $(THEME)
	cp $(lastword $(subst -, ,$(THEME))).xml $(THEME)/
	cp oxygen.svg $(THEME)
	cp screenshot.png $(THEME)

background:
	mkdir -p $(THEME)
	inkscape --without-gui \
		 --export-width=1920 \
		 --export-height=1200 \
		 --export-png="$(THEME)/background.png" \
			$@.svg

fred:
	mkdir -p $(THEME)
	inkscape --without-gui \
		 --export-width=94 \
		 --export-height=100 \
		 --export-png="$(THEME)/$@.png" \
			$@.svg

clean:
	$(RM) -r $(THEME)
