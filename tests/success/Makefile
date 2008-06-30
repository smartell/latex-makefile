
TESTS= \
  article \
  article-include \
  beamer \
  bibunits \
  glossary-bib \
  graphics-latex \
  graphics-pdftex \
  index \
  minitoc-partchap \
  minitoc-sect \
  multiple-documents \
  natbib \
  thumbpdf
# beamer_handouts

PURGETESTS:=$(foreach test,$(TESTS),$(test).purge)
CLEANTESTS:=$(foreach test,$(TESTS),$(test).clean)

.PHONY: all purge clean $(TESTS) $(PURGETESTS) $(CLEANTESTS)

all: $(TESTS)

purge: $(PURGETESTS)

clean: $(CLEANTESTS)


$(PURGETESTS): %.purge:
	cd $* && make -s purge

$(CLEANTESTS): %.clean:
	cd $* && make -s clean

$(TESTS):
	cd $@ && make -s