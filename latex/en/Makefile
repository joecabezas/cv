IMAGE=blang/latex:ubuntu
COMPILER=pdflatex

pdf: cv.pdf

cv.pdf: cv.tex
	docker run --rm -i --user="$(id -u):$(id -g)" --net=none -v $(PWD):/data $(IMAGE) $(COMPILER) $^

clean:
	rm cv.aux cv.bbl cv.blg cv.log cv.out
