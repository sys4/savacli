# generate savacli Documentation from ASCIIDOC files
# requeries "asciidoctor" (https://asciidoctor.org/) and
# "asciidoctor-pdf" (https://asciidoctor.org/docs/asciidoctor-pdf/)
#
CONVERTER    = asciidoctor
PDFCONVERTER = asciidoctor-pdf


all: html pdf manpage

.PHONY: clean pdf manpage html

%.pdf: %.adoc
		$(PDFCONVERTER) $<

pdf: savacli.5.pdf

%.5: %.5.adoc
		$(CONVERTER) -b manpage $<

manpage: savacli.5

%.html: %.adoc
		$(CONVERTER) $<

html: savacli.5.html

clean:
		rm -f *.html *.pdf *.5
