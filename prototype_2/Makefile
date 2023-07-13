.PHONY: clean all

all: fab/gerbers.zip

fab:
	mkdir -p fab

fab/gerbers.zip: prototype_1.kicad_pcb fab prototype_1.sch
	kikit fab jlcpcb --assembly --schematic prototype_1.sch \
		--ignore J4,J5,J6,H5,H6,H7,H8,U4,J1,J2,J3,J7,J8,J9,J10,J11,J12,J14,J15,J16 \
		$< fab

clean:
	rm -rf fab
