FILENAME=slides
TMPDIRNAME=tmp
SRCDIR=.
TMPDIR=${SRCDIR}/${TMPDIRNAME}
FLAGS=-output-directory ${TMPDIR}

build: *.tex 
	mkdir -p ${TMPDIR}
	pdflatex ${FLAGS} ${FILENAME}.tex
	pdflatex ${FLAGS} ${FILENAME}.tex
	mv -f ${TMPDIR}/${FILENAME}.pdf ${SRCDIR}/

clean:
	rm -rf ${TMPDIR}
