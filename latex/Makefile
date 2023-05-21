IMAGE=blang/latex:ubuntu
COMPILER=pdflatex

en: en/cv.pdf

en/cv.pdf: en/cv.tex
	docker run --rm -i --user="$(id -u):$(id -g)" --net=none -v "$(PWD)":/data "$(IMAGE)" $(COMPILER) $^
	mv cv.pdf $@
