all: doc-html doc-pdf

output-dir:
	mkdir -p output

doc-html: output-dir
	asciidoctor --safe -b html5 -B ./src/ -D output -o lsp-mode.html ./src/index.adoc
	cp ./src/output/* ./output/

doc-pdf: output-dir
	asciidoctor-pdf  --safe -b html5 -B ./src/ -D output -o lsp-mode.pdf ./src/index.adoc
	cp ./src/output/* ./output/

clean:
	rm -rf ./src/output output

.DEFAULT_GOAL: all
