FILENAME=slides
BIBFILE=references
TMPDIRNAME=tmp
SRCDIR=.
TMPDIR=${SRCDIR}/${TMPDIRNAME}
BIBDIR=${SRCDIR}/../references
FLAGS=-output-directory ${TMPDIR}

build: *.tex ${BIBDIR}/${BIBFILE}.bib
	mkdir -p ${TMPDIR}
	pdflatex ${FLAGS} ${FILENAME}.tex
	bibtex ${TMPDIR}/${FILENAME}.aux
	pdflatex ${FLAGS} ${FILENAME}.tex
	pdflatex ${FLAGS} ${FILENAME}.tex
	mv -f ${TMPDIR}/${FILENAME}.pdf ${SRCDIR}/

clean:
	rm -rf ${TMPDIR}

distclean: clean
	rm -f *.pdf
