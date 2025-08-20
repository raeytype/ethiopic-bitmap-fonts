
#
#  This works with GNU Make, I'm not sure about others...
#
#  Try at the command line:  make
#                         :  make install
#

TOPCF = bdftopcf 
Z = compress    
BFONTS = fidel11.bdf fidel12.bdf fidel15.bdf fidel18.bdf fidel20.bdf 
PFONTS = $(BFONTS:.bdf=.pcf)

all: ${PFONTS}

${PFONTS}:  $(BFONTS)

install:
	mkfontdir
	xset fp+ `pwd`

%.pcf : %.bdf
	$(TOPCF)  $< > $@
	$(Z) $@

