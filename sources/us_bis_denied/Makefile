URL=https://www.bis.doc.gov/dpl/dpl.txt
WORK_PATH=$(OPENNAMES_SOURCE_DATA)
TXT_FILE=$(WORK_PATH)/us_bis_denied.csv

all: scrape parse

$(TXT_FILE):
	mkdir -p $(WORK_PATH)
	curl -o $(TXT_FILE) $(URL)

scrape: $(TXT_FILE)

parse: $(TXT_FILE)
	python parse.py $(TXT_FILE)

clean:
	rm $(TXT_FILE)
