LOGS=base.log IQBT.log
OUTPUT= \
	beamercolorthemefibeamer-fcfm.sty	beamerfontthemefibeamer-fcfm.sty \
	beamerinnerthemefibeamer-fcfm.sty beamerouterthemefibeamer-fcfm.sty \
	beamercolorthemefibeamer-fcfm-IQBT.sty \

.PHONY: explode implode clean all
all: explode
explode: $(LOGS)

%.log: %.ins %.dtx
	xetex $<

implode:
	rm -f $(OUTPUT) $(LOGS)
