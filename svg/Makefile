ALL_SVG = $(shell ls *.svg)
ALL_PNG = $(subst .svg,.png,$(ALL_SVG))

all: $(ALL_PNG)

info:
	@echo 'Makefile: Known local svg-Files:'
	@echo ''
	@echo $(shell for file in $(ALL_SVG); do echo $$file;done)

%.png: %.svg
	inkscape --file=$< --export-area-drawing --without-gui --export-png=$@

clean:
	@echo 'Makefile: doing $@'
	$(shell for file in $(ALL_PNG); do rm -f $$file;done)

.PHONY: clean
