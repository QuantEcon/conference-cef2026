# Build the CEF 2026 talk (reveal.js) from Markdown.
#
# Requires: Quarto (https://quarto.org). Already installed on this machine.
#
# Usage:
#   make            # render slides.html (self-contained)
#   make preview    # live-reloading preview in the browser
#   make pdf         # print-to-PDF instructions (see README)
#   make clean

QUARTO := quarto

SRC    := slides.qmd
HTML   := slides.html
THEME  := theme/quantecon.scss

.PHONY: all preview pdf clean

all: $(HTML)

$(HTML): $(SRC) $(THEME) assets/qe-logo-large.png
	$(QUARTO) render $(SRC) --to revealjs

preview:
	$(QUARTO) preview $(SRC) --to revealjs

pdf: $(HTML)
	@echo "To export a PDF for the conference laptop:"
	@echo "  1. open slides.html in Chrome and append ?print-pdf to the URL"
	@echo "  2. File > Print > Save as PDF (Background graphics ON, margins None)"
	@echo "Or, with decktape installed:  decktape reveal slides.html slides.pdf"

clean:
	rm -rf $(HTML) slides_files .quarto
