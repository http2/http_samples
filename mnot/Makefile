
compare=../../compression-test/compare_compressors.py
codecs=-c spdy3 -c delta -c simple

hars = $(wildcard *.har)
tsvs := $(hars:%.har=%-req.tsv)

all: $(tsvs) index.txt
	@echo $<

%-req.tsv: %.har
	$(compare) $(codecs) $< -t --prefix=$(subst req,,$(basename $@))

index.txt:
	@echo $(hars:%.har=%) > index.txt

clean:
	rm *.tsv index.txt