WORK_PATH=$(OPENNAMES_SOURCE_DATA)/zz_every_politician

all: scrape parse

$(WORK_PATH):
	mkdir -p $(WORK_PATH)
	python scrape.py $(WORK_PATH)

scrape: $(WORK_PATH)

parse: $(WORK_PATH)
	python parse.py $(WORK_PATH)

clean:
	rm -rf $(WORK_PATH)
