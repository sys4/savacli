# generate savacli Documentation from ASCIIDOC files
# requeries "asciidoctor" (https://asciidoctor.org/) and
# "asciidoctor-pdf" (https://asciidoctor.org/docs/asciidoctor-pdf/)
#
CONVERTER=asciidoctor
PDFCONVERTER=asciidoctor-pdf

all: html pdf manpage

pdf: savacli.5.pdf

%.pdf: %.adoc
		$(PDFCONVERTER) $<

manpage: savacli.5

%.5: %.adoc
		$(CONVERTER) -b manpage $<

html: savacli.5.html

%.html: %.adoc
		$(CONVERTER) $<

clean:
		rm -f *.html *.pdf *.5
