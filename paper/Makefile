FILENAME=Cloud_Privacy
BIBFILE=Cloud_Privacy
TMPDIRNAME=tmp
SRCDIR=.
TMPDIR=${SRCDIR}/${TMPDIRNAME}
BIBDIR=${SRCDIR}
FLAGS=-output-directory ${TMPDIR}

build: *.tex ${BIBDIR}/${BIBFILE}.bib
	mkdir -p ${TMPDIR}
	pdflatex ${FLAGS} ${FILENAME}.tex
	bibtex ${TMPDIR}/${FILENAME}.aux
	pdflatex ${FLAGS} ${FILENAME}.tex
	pdflatex ${FLAGS} ${FILENAME}.tex
	cp ${TMPDIR}/${FILENAME}.pdf ${SRCDIR}/

clean:
	rm -rf ${TMPDIR}

distclean: clean
	rm -f *.pdf

