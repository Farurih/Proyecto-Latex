PHONY: all implode
TARGETS=expected-IQBT-lualatex.pdf expected-IQBT-pdflatex.pdf 

EXAMPLEDIR=../../example/fcfm

# This target runs all the tests.
all:
	make -C $(EXAMPLEDIR) implode
	make -C $(EXAMPLEDIR) all
	make $(TARGETS)

# This target runs a single test.
expected-%.pdf: $(EXAMPLEDIR)/%.pdf
	../comparepdf.sh $< $@ || \
	{ [ "$(UPDATE_FAILED)" = true ] && mv $< $@; }

# This is a dummy target.
implode:
	
